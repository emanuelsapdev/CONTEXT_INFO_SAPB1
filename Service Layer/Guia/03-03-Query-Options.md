# 3.6 Query Options

> Source: *Working with SAP Business One Service Layer* v1.29, section 3.6 (paraphrased technical reference).
>
> **Resumen (ES):** filtros, selección de campos, orden, paginación, conteos, agregaciones (`$apply`), agrupación, `$crossjoin`, filtros a nivel de línea con `QueryService_PostQuery` y `$expand` con `$select`.

## Supported query options

| Option | Purpose | Example | Propósito (ES) |
|---|---|---|---|
| `$filter` | Filter a collection | `/Orders?$filter=DocTotal gt 3000` | Filtrar |
| `$select` | Return only some properties | `/Orders?$select=DocEntry,DocTotal` | Elegir campos |
| `$orderby` | Sort | `/Orders?$orderby=DocTotal asc, DocEntry desc` | Ordenar |
| `$top` | First *n* records | `/Orders?$top=3` | Primeros n |
| `$skip` | Skip *n* records (applied **before** `$top`, regardless of order in URL) | `/Orders?$top=3&$skip=2` | Saltar n |
| `$count` | Count of a collection | `/Orders/$count`, `/Items/$count?$filter=ItemCode eq 'test'` | Contar |
| `$inlinecount` | Total count inline with results (**OData v3 only**, 9.1 PL06+) | `/Banks?$inlinecount=allpages` | Conteo junto a resultados (solo v3) |
| `$apply` | Aggregation / grouping / pre-filter | `/Orders?$apply=aggregate(DocRate with sum as Total)` | Agregar/agrupar |
| `$expand` | Expand navigation properties (with nested `$select` since FP 2105) | `/ServiceCalls(1)?$expand=BusinessPartner($select=CardCode)` | Expandir relaciones |

### `$filter` functions and operators

| Type | Supported | Soportado (ES) |
|---|---|---|
| Functions | `startswith`, `endswith`, `contains`, `substringof` | Funciones de texto |
| Logical | `and`, `or`, `not` (not since 9.1 PL01), parentheses | Lógicos |
| Relational | `eq`, `ne`, `lt`, `le`, `gt`, `ge` | Comparación |

```http
/Orders?$filter=DocEntry lt 8 and (DocEntry lt 8 or DocEntry gt 116) and CardCode eq 'c1'
/Orders?$filter=DocEntry lt 8 and ((DocEntry lt 8 or DocEntry gt 116) and startswith(CardCode,'c1'))
/Items?$filter=not (startswith(ItemName, 'item') and ForeignName eq null)
```

## 3.6.1–3.6.5 Common patterns

| Need | Request | Necesidad (ES) |
|---|---|---|
| All entities | `GET /Items` or `GET /Items?$select=*` | Todos los registros |
| Some fields of one entity | `GET /Items('i1')?$select=ItemCode,ItemName,ItemPrices` | Algunos campos de una entidad |
| Enum filter (value or name) | `GET /BusinessPartners?$filter=CardType eq 'C'` ≡ `... eq 'cCustomer'` | Filtrar enum por valor o nombre |
| Date filter | `DocDate eq '2014-04-23'`, `'20140423'`, `datetime'2014-04-23'`, `datetime'20140423'`, `'2014-04-23T12:21:21'`, `'20140423000000'` (time part ignored) | Fechas: varios formatos, se ignora la hora |
| Time filter | `DocTime eq '18:38:00'`, `'18:38'`, `'183800'`, `'1838'`, `'2014-06-18T18:38:00Z'`, `'2014-06-18T18:38'` (only hour/minute used) | Horas: solo hora y minuto |

## 3.6.6 Pagination

`GET /Orders` returns 20 records plus a next link:

```json
{ "value": [ {"DocEntry": 7, ...}, ..., {"DocEntry": 26, ...} ],
  "odata.nextLink": "/b1s/v1/Orders?$skip=20" }
```

| Item | Detail | Detalle (ES) |
|---|---|---|
| Next-link annotation | `odata.nextLink` (v3) / `@odata.nextLink` (v4) | Enlace a la siguiente página |
| Default page size | 20 | Tamaño por defecto: 20 |
| Change globally | `PageSize` in `conf/b1s.conf` | Configuración global |
| Change per request | Header `Prefer: odata.maxpagesize=50` → response header `Preference-Applied: odata.maxpagesize=50` | Por request (tiene prioridad) |
| Disable paging | `PageSize=0` or `odata.maxpagesize=0` | 0 = sin paginación |

## 3.6.7 Aggregation (`$apply=aggregate(...)`)

Available since 9.1 PL12 for HANA. Each aggregate needs an alias (`as Alias`), which becomes a dynamic property in the result.

| Method | Example | Equivalent SQL | Método (ES) |
|---|---|---|---|
| `sum` | `/Orders?$apply=aggregate(DocRate with sum as TotalDocRate)` | `SELECT SUM(T0."DocRate") AS "TotalDocRate" FROM "ORDR" T0` | Suma |
| `average` | `/Orders?$apply=aggregate(VatSum with average as AvgVatSum)` | `SELECT AVG(T0."VatSum") ...` | Promedio |
| `max` | `aggregate(DocEntry with max as MaxDocEntry)` | `SELECT MAX(...)` | Máximo |
| `min` | `aggregate(DocEntry with min as MinDocEntry)` | `SELECT MIN(...)` | Mínimo |
| `countdistinct` | `aggregate(CardCode with countdistinct as CountDistinctCardCode)` | `SELECT COUNT(DISTINCT T0."CardCode") ...` | Conteo de distintos |
| `$count` (virtual property; alias only, no method) | `aggregate($count as OrdersCount)` | `SELECT COUNT(T0."DocEntry") ...` | Conteo |

Response shape: `{ "odata.metadata": "$metadata#Orders(TotalDocRate)", "value": [ { "odata.id": null, "TotalDocRate": 4.0 } ] }`.

### `$inlinecount` (OData v3)

- Allowed values: `allpages` (return total count in `odata.count`) or `none`/absent. Any other value → `400 Bad Request`.
- Works with `$top` and `$filter`:

```http
GET /Banks?$inlinecount=allpages&$top=2         → "odata.count": "5" + first 2 banks
GET /Banks?$inlinecount=allpages&$filter=BankCode gt 'bank003'   → "odata.count": "2"
```

(In OData v4 use `$count=true`.)

## 3.6.8 Grouping (`groupby`, 9.2 PL03+ HANA)

| Variant | Request | Equivalent SQL | Variante (ES) |
|---|---|---|---|
| Simple group | `/Orders?$apply=groupby((CardCode, DocEntry))` (also `groupby((Orders/CardCode, Orders/DocEntry))`) | `SELECT CardCode, DocEntry FROM ORDR GROUP BY CardCode, DocEntry` | Agrupación simple |
| Group + aggregate | `/Orders?$apply=groupby((CardCode), aggregate(DocNum with sum as TotalDocNum))` | `SELECT CardCode, SUM(DocNum) ... GROUP BY CardCode` | Agrupación con agregación |
| Filter then group (transformations separated by `/`) | `/Orders?$apply=filter(Orders/CardCode eq 'c001')/groupby((CardCode), aggregate(DocNum with sum as TotalDocNum))` | `... WHERE CardCode='c001' GROUP BY CardCode` | Filtrar y luego agrupar |
| Equivalent with `$filter` | `...$apply=groupby(...)&$filter=(Orders/CardCode ne 'c001')` | — | Variante con $filter |

A property path must not appear twice in `groupby`.

## 3.6.9 Cross-joins (`$crossjoin`, 9.2 PL07+ HANA)

Join entity sets that have no navigation property defined.

```http
GET /b1s/v1/$crossjoin(Orders,BusinessPartners)?$expand=Orders($select=DocEntry,DocNum),BusinessPartners($select=CardCode)
    &$filter=Orders/CardCode eq BusinessPartners/CardCode and Orders/DocNum le 3 and startswith(BusinessPartners/CardCode,'c00')
```

Result: `"value": [ { "BusinessPartners": {"CardCode": "c002"}, "Orders": {"DocEntry": 3, "DocNum": 2} }, ... ]` — equivalent to `SELECT ... FROM ORDR T0, OCRD T1 WHERE T0.CardCode = T1.CardCode AND ...`.

| Feature | Example | Función (ES) |
|---|---|---|
| More than two sets | `$crossjoin(Orders,BusinessPartners,Activities)?$expand=...&$filter=Orders/CardCode eq BusinessPartners/CardCode and BusinessPartners/CardCode eq Activities/CardCode` | Más de dos entidades |
| Arithmetic (`add`, `sub`, `mul`, `div`) in `$select` and `$filter` | `$expand=Orders($select=DocEntry mul (DocNum sub 1) as DocSeq),...&$filter=... and Orders/DocEntry ge Orders/DocNum sub 3` | Cálculos |
| Aggregation | `$crossjoin(Orders,BusinessPartners)?$apply=filter(Orders/CardCode eq BusinessPartners/CardCode)/groupby((BusinessPartners/CardCode, Orders/DocEntry),aggregate(Orders(DocNum with countdistinct as DistinctDocNum)))` | Agregaciones |
| max | `...aggregate(Orders(DocNum with max as MaxDocNum))` | Máximo |
| count | `...aggregate(Orders/$count as CountDocEntry)` | Conteo |

A bare `$crossjoin(Orders,BusinessPartners)` without options is rejected: `{"error":{"code":-1000,"message":{"value":"invalid $crossjoin query"}}}`.

## 3.6.10 Row-level filter — `QueryService_PostQuery` (9.2 PL11+ HANA)

To filter on document **lines** (not possible with plain `$filter` on the header), SL exposes a query service built on `$crossjoin` that separates the path and the options:

```xml
<FunctionImport Name="QueryService_PostQuery" ReturnType="Edm.String" m:HttpMethod="POST">
  <Parameter Name="QueryOption" Type="Edm.String"/>
  <Parameter Name="QueryPath" Type="Edm.String"/>
</FunctionImport>
```

```http
POST /b1s/v1/QueryService_PostQuery
{
  "QueryPath": "$crossjoin(Orders,Orders/DocumentLines)",
  "QueryOption": "$expand=Orders($select=DocEntry, DocNum),Orders/DocumentLines($select=ItemCode,LineNum)&$filter=Orders/DocEntry eq Orders/DocumentLines/DocEntry and Orders/DocEntry ge 3 and Orders/DocumentLines/LineNum eq 0"
}
```

Result rows look like `{ "Orders": {"DocEntry": 9, "DocNum": 5}, "Orders/DocumentLines": {"ItemCode": "i1", "LineNum": 0} }`. Parentheses work in the filter (e.g. `(LineNum eq 0 or LineNum eq 1 or LineNum eq 2)`).

The response is a **raw string (`text/plain`) shaped like JSON** — parse it with a JSON library.

## 3.6.11 `$expand` enhancements (FP 2105+)

`$select` can be nested inside `$expand`, for a single entity or for each entity of a collection.

```http
GET /b1s/v2/ServiceCalls(1)?$expand=BusinessPartner($select=ContactPerson, CardCode),Item($select=ItemCode, ItemName)&$select=Subject
```

```json
{ "@odata.context": ".../$metadata#ServiceCalls/$entity",
  "BusinessPartner": { "CardCode": "c1", "ContactPerson": "contact001" },
  "Item": { "ItemCode": "i001", "ItemName": "i001 name" },
  "Subject": "subject1" }
```

Equivalent forms (same result):

```http
...?$expand=BusinessPartner($select=ContactPerson, CardCode),Item&$select=Item/ItemCode, Item/ItemName, Subject
...?$expand=BusinessPartner,Item&$select=BusinessPartner/ContactPerson, BusinessPartner/CardCode, Item/ItemCode, Item/ItemName, Subject
```

The same works on a collection (`GET /b1s/v2/ServiceCalls?$expand=...`): every element of `value` contains the expanded objects.
