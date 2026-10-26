# 3.19 JavaScript Extensions (server-side scripting)

> Source: *Working with SAP Business One Service Layer* v1.29, section 3.19 (paraphrased technical reference).
>
> **Resumen (ES):** extensiones en JavaScript ejecutadas dentro del Service Layer (motor V8): funciones de entrada por verbo HTTP, URL de scripts, SDK (request/response, CRUD, consultas, transacciones, excepciones), logs, generador del SDK, despliegue vía Extension Manager y casos típicos.

Available since **9.2 PL04**.

## 3.19.1–3.19.2 Engine and framework

- Engine: **Google V8** (fast, and C++ like SL itself).
- Layers: V8 inside SL → **C++/JavaScript interop layer** → **JavaScript SDK** (high-level API that minimizes costly context switches between C++ and JS) → your extension. Build extensions on top of the SDK.

## 3.19.3 Entry functions

A script defines functions named after the HTTP verbs; the one matching the request's verb runs. **Names must be upper case.**

```javascript
function GET()    { ... }
function POST()   { ... }
function PATCH()  { ... }
function DELETE() { ... }
```

## 3.19.4 URL mapping

```
/b1s/v1/script/{partner name}/{script name}
/b1s/v2/script/{partner name}/{script name}
```

Example: `POST /b1s/v1/script/mtcsys/items` runs `POST()` in the script registered as `items` by partner `mtcsys`. The script and its `.ard` file must be deployed to SLD (see 3.19.8).

## 3.19.5 JavaScript SDK

Designed like a statically typed library (good IntelliSense), follows CommonJS / Node.js style (`require`). Recommended IDE in the guide: Visual Studio with the Node.js plug-in.

### HTTP request API (`HttpModule.js` → `http.request`)

| Function | Returns | Devuelve (ES) |
|---|---|---|
| `getContent()` | Raw request payload | Cuerpo crudo |
| `getJsonObj()` / `getJsonObject()` | Payload parsed as JSON | Cuerpo como JSON |
| `getMethod()` | HTTP verb | Verbo HTTP |
| `getContentType()` | MIME type of the body | Tipo MIME |
| `getParameter(name)` | Query parameter value or `null` | Parámetro de la URL |
| `getParameterNames()` | Array of parameter names | Nombres de parámetros |
| `getEntityKey()` | Entity key from the URL (e.g. `'i001'`) | Clave de la entidad |
| `getHeader(name)` | Request header value | Cabecera |

### HTTP response API (`http.response`)

| Function | Purpose | Propósito (ES) |
|---|---|---|
| `setHeader(name, value)` | Add a header | Agregar cabecera |
| `setContentType(type)` | Response content type (e.g. `http.ContentType.APPLICATION_JSON`) | Tipo de contenido |
| `setCharSet(charset)` | Charset (e.g. UTF-8) | Juego de caracteres |
| `setStatus(status)` | Status code (e.g. `http.HttpStatus.HTTP_OK`) | Código de estado |
| `setContent(content)` | Body | Cuerpo |
| `send(status, content)` | Send response (args optional) | Enviar |

`require` imports a module; `http.request`/`http.response` are pre-created instances; the module also exports constants `HttpStatus`, `ContentType` and the `ScriptException` class.

```javascript
var http = require('HttpModule.js');
function PATCH() {   // PATCH /b1s/v1/script/mtcsys/items('i001')?key1=val1&key2=val2
  var ret = {};
  ret.content = http.request.getJsonObj();
  ret.method = http.request.getMethod();
  ret.dataServiceVersion = http.request.getHeader("DataServiceVersion");
  ret.paramNames = http.request.getParameterNames();
  (ret.paramNames || []).forEach(function (p) { ret[p] = http.request.getParameter(p); });
  ret.key = http.request.getEntityKey();               // "'i001'"
  http.response.setContentType(http.ContentType.APPLICATION_JSON);
  http.response.setStatus(http.HttpStatus.HTTP_OK);
  http.response.setContent(ret);
  http.response.send();
}
```

### Entity CRUD API (`ServiceLayerContext.js`)

| Style | Functions | When | Estilo (ES) |
|---|---|---|---|
| On an `EntitySet` (`slContext.Items`) | `add(content, cb)`, `get(key, cb)`, `update(content, key, cb)`, `remove(key, cb)` | Entity name known in advance | Con entity set conocido |
| On `ServiceLayerContext` | `add(name, content, cb)`, `get(name, key, cb)`, `update(name, content, key, cb)`, `remove(name, key, cb)` | Name dynamic or a UDO | Nombre dinámico o UDO |

Results expose `isOK()`, `operation`, `status`, `body`, `getErrMsg()`. Typed classes are available, e.g. `require('EntityType/Item.js')`, `require('EntityType/Document.js')` (`new Order.DocumentLine()`, `Order.DocumentLineCollection`, `Item.create(body)` to convert a plain object).

```javascript
var ServiceLayerContext = require('ServiceLayerContext.js');
var Item = require('EntityType/Item.js');
var http = require('HttpModule.js');
function POST() {
  var sl = new ServiceLayerContext(), ret = [];
  var item = new Item(); item.ItemCode = "i001";
  var r = sl.Items.add(item);
  if (!r.isOK()) throw http.ScriptException(http.HttpStatus.HTTP_BAD_REQUEST, "create entity failure");
  ret.push({ operation: r.operation, status: r.status });          // add 201
  r = sl.Items.get("i001");                                         // get 200
  item.ItemName = 'new_item_name';
  r = sl.update("Items", item, "i001");                             // update 204
  r = sl.remove("Items", "i001");                                   // remove 204
  http.response.send(http.HttpStatus.HTTP_OK, ret);
}
```

### Entity query API

| On | Functions | En (ES) |
|---|---|---|
| `EntitySet` | `query(queryOption, isCaseInsensitive)`, `count(queryOption, isCaseInsensitive)` | Entity set |
| `ServiceLayerContext` | `query(name, queryOption, isCaseInsensitive)`, `count(name, queryOption, isCaseInsensitive)` | Contexto |

- `isCaseInsensitive` only matters on **HANA** (case-sensitive by default because of its Unicode collation); case-insensitive queries are slower. Supported since 9.2 PL07 (HANA).
- Results: `.toArray()`.

```javascript
var q = "$select=CardName, CardCode & $filter=contains(CardCode, 'c1') & $top=5 & $orderby=CardCode";
var cs = sl.BusinessPartners.query(q);                 // case-sensitive
var ci = sl.query("BusinessPartners", q, true);         // case-insensitive
```

The same is available for normal REST calls with the header **`B1S-CaseInsensitive: true`**, e.g. `GET /b1s/v1/BusinessPartners?$filter=contains(CardCode, 'c2')&$select=CardCode` returns `C20000`, `C23900`, `c21`, `c22`.

### Transaction API

| Function | Purpose | Propósito (ES) |
|---|---|---|
| `startTransaction()` | Begin | Iniciar |
| `commitTransaction()` | Commit | Confirmar |
| `rollbackTransaction()` | Roll back | Revertir |
| `isInTransaction()` | True if inside a transaction | ¿Dentro de una transacción? |

- Always pair `start` with `commit` or `rollback`.
- **Maximum 10 operations per transaction** (big transactions hurt throughput).

```javascript
function POST() {
  var sl = new ServiceLayerContext(), list = http.request.getJsonObj();
  if (!(list instanceof Array)) throw http.ScriptException(http.HttpStatus.HTTP_BAD_REQUEST, "invalid format of payload");
  sl.startTransaction();
  for (var i = 0; i < list.length; ++i) {
    var r = sl.BusinessPartners.add(list[i]);
    if (!r.isOK()) { sl.rollbackTransaction(); throw http.ScriptException(http.HttpStatus.HTTP_BAD_REQUEST, r.getErrMsg()); }
  }
  sl.commitTransaction();
  http.response.setContentType(http.ContentType.TEXT_PLAIN);
  http.response.send(http.HttpStatus.HTTP_OK, "transaction committed");
}
```

### Exceptions

| Type | Error code | Example message | Tipo (ES) |
|---|---|---|---|
| Compile error | `511` | `Script error: compile error [SyntaxError: Unexpected token ;].` | Error de compilación |
| Runtime error | `512` | `Script error: runtime error [ReferenceError: Bank is not defined].` | Error de ejecución |
| User exception (`throw new http.ScriptException(status, msg)`) | `600` + chosen HTTP status | e.g. `404` "the given order not found" | Excepción del usuario |

## 3.19.6 Logging

No debugger. Use `console.log('...')`; output goes to `{SL install path}/logs/script/`.

## 3.19.7 SDK generator — `Metadata2JavaScript`

Generates the typed SDK from metadata (objects change between patches). Shipped in SL's `bin` folder; needs a Java JRE (Linux: `export JAVA_HOME=/usr/sap/SAPBusinessOne/Common/sapjvm_8/jre; export PATH=$JAVA_HOME/bin:$PATH`). On Windows (since FP 2011) run it as `java -jar Metadata2JavaScript.jar ...`.

| Source | Command | Origen (ES) |
|---|---|---|
| Local metadata file | `Metadata2JavaScript -a metadata.xml -o ./output` (`--addr`, `--output`; default output `./b1s_sdk`) | Archivo local |
| Remote SL | `Metadata2JavaScript --addr https://dbserver:50000/b1s/v1/ --user manager --password 1234 --company SBODEMOUS` (`-u`, `-p`, `-c`) | SL remoto |

## 3.19.8 Deployment (Extension Manager / SLD)

1. Create an `.ard` descriptor (e.g. `Items.ard`), `Type="ServiceLayerScript"`:

   ```xml
   <?xml version="1.0" encoding="utf-8"?>
   <AddOnRegData SlientInstallation="" SlientUpgrade="" Partnernmsp="mtcsysnm" SchemaVersion="3.0"
                 Type="ServiceLayerScript" OnDemand="" OnPremise="" ExtName="ItemsExt" ExtVersion="1.00"
                 Contdata="sa" Partner="mtcsys" DBType="HANA" ClientType="S">
     <ServiceLayerScripts><Script Name="items" FileName="Items.js"></Script></ServiceLayerScripts>
     <XApps><XApp Name="" Path="" FileName="" /></XApps>
   </AddOnRegData>
   ```

2. Zip the `.ard` and the `.js` (e.g. `Items.zip`).
3. Import it in the Extension Manager (**Extension Import Wizard**).
4. Assign it to a company (**Extension Assignment Wizard**).
5. Call `/b1s/v1/script/mtcsys/items` (partner + script name).

Notes: one `.ard` can't bundle multiple script files; don't use `test` as `Partner` (reserved); see *How to Package and Deploy SAP Business One Extensions for Lightweight Deployment*.

## 3.19.9 Typical use cases

| Use case | Description | Caso (ES) |
|---|---|---|
| Complex transactions | E.g. create a sales order and a delivery based on it (`BaseType = 17`, `BaseEntry = newOrder.DocEntry`, `BaseLine = n`) in one transaction — not possible with `$batch` because the delivery needs the order's `DocEntry` | Transacciones complejas |
| Custom business logic for UDOs | E.g. before adding `MyOrder`: check each item exists and has enough `QuantityOnStock`, compute `U_DocTotal = Σ U_Price × U_Quantity`, then `slContext.add("MyOrder", myOrder)` | Lógica de negocio para UDOs |

## 3.19.10 Calling scripts from .NET

Script responses are free-form, so there is no fixed metadata and WCF alone can't consume them. Use `HttpWebRequest`/`HttpClient` plus JSON serialization (e.g. Newtonsoft): POST to `new Uri(baseUri, "script/<partner>/<script>")` with the `Cookie` header (B1SESSION), `Content-Type: application/json;odata=minimalmetadata`, then deserialize the response (e.g. into the WCF-generated `Document` class).
