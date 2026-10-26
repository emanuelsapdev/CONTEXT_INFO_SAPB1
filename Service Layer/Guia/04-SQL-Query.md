# 4. SQL Query (`SQLQueries`)

> Source: *Working with SAP Business One Service Layer* v1.29, chapter 4 (paraphrased technical reference).
>
> **Resumen (ES):** ejecutar consultas SQL de solo lectura (un subconjunto de SQL) guardadas como entidades `SQLQueries`, con parámetros, paginación, lista blanca de tablas/columnas, normalización HANA/SQL Server, errores, permisos y seguridad.

Since **SAP Business One 10.0 FP 2011**, on SQL Server and HANA. Goals: query data not exposed via OData, more dynamic and lighter than deploying Semantic Layer/SQL views, with a familiar SQL subset (no new query language).

## 4.1 Metadata

```xml
<EntityType Name="SQLQuery">
  <Key><PropertyRef Name="SqlCode"/></Key>
  <Property Name="SqlCode" Nullable="false" Type="Edm.String"/>
  <Property Name="SqlName" Type="Edm.String"/>
  <Property Name="SqlText" Type="Edm.String"/>
  <Property Name="ParamList" Type="Edm.String"/>
  <Property Name="CreateDate" Type="Edm.DateTime"/>
  <Property Name="UpdateDate" Type="Edm.DateTime"/>
</EntityType>
<EntitySet EntityType="SAPB1.SQLQuery" Name="SQLQueries"/>
<FunctionImport IsBindable="true" Name="List" ReturnType="SAPB1.SQLQueryResult">
  <Parameter Name="SQLQueryParams" Type="SAPB1.SQLQuery"/>
  <Parameter Name="ParamList" Type="Edm.String"/>
</FunctionImport>
```

| Property | Meaning | Significado (ES) |
|---|---|---|
| `SqlCode` | Key / unique ID of the query | Clave de la consulta |
| `SqlName` | Descriptive name | Nombre descriptivo |
| `SqlText` | SQL text (stored normalized for the DB) | Texto SQL (se guarda normalizado) |
| `ParamList` | Detected parameter names (comma-separated), e.g. `docTotal` | Parámetros detectados |
| `CreateDate` / `UpdateDate` | Audit dates | Fechas de auditoría |

`SQLQueries` supports **ETag** (`odata.etag` in responses).

## 4.2 CRUD

| Operation | Request | Operación (ES) |
|---|---|---|
| Create | `POST /b1s/v1/SQLQueries` `{"SqlCode": "sql04", "SqlName": "queryOnItem", "SqlText": "select ItemCode, ItemName, ItmsGrpCod from oitm"}` → `201`, `SqlText` returned normalized: `select [ItemCode], [ItemName], [ItmsGrpCod] from [OITM]` | Crear |
| Read by key | `GET /b1s/v1/SQLQueries('sql04')` | Leer |
| Update | `PATCH /b1s/v1/SQLQueries('sql04')` `{"SqlName": "queryOnItem", "SqlText": "select ItemCode, ItemName from oitm"}` → `204` | Actualizar |
| Delete | `DELETE /b1s/v1/SQLQueries('sql04')` → `204` | Borrar |
| List all | `GET /b1s/v1/SQLQueries` (paged; `Prefer: odata.maxpagesize=5` → `odata.nextLink: "SQLQueries?$skip=5"`) | Listar |

## 4.3–4.4 Running a query — bound function `List`

```http
GET  /b1s/v1/SQLQueries('sql04')/List
POST /b1s/v1/SQLQueries('sql04')/List
```

Returns the columns of the `SELECT`:

```json
{ "odata.metadata": ".../$metadata#SAPB1.SQLQueryResult",
  "SqlText": "select [ItemCode], [ItemName], [ItmsGrpCod] from [OITM]",
  "value": [ { "ItemCode": "i001", "ItemName": "i001", "ItmsGrpCod": 100 }, ... ] }
```

**Paging is mandatory** for `List` (protects the server from huge results/unfiltered joins). Change the page size with `Prefer: odata.maxpagesize=<n>`; next page in `odata.nextLink` (e.g. `SQLQueries('sql0001')/List?&$skip=5`). Underlying SQL: SQL Server wraps in `SELECT * FROM (...) B1S_DUMMY_TABLE ORDER BY CURRENT_TIMESTAMP OFFSET 0 ROWS FETCH NEXT 5 ROWS ONLY`; HANA appends `LIMIT 5 OFFSET 0`.

## 4.5 Allowlist (security)

### 4.5.1 Table allowlist

Only tables in **`<SL install>/conf/b1s_sqltable.conf`** (JSON) can be queried. You may remove tables to tighten security; **adding tables not on the list is unsupported** and may compromise security.

| Area | Tables | Área (ES) |
|---|---|---|
| Company / admin | CINF, OADM, ADM1, OADP, OCRN | Sociedad / administración |
| Business partners | OCRD, OCRP, CRD1, OCPR (contact persons) | Socios de negocios |
| Sales documents | OQUT+QUT1-14, ORDR+RDR1-14, ODLN+DLN1-14, ORRR+RRR1-14, ORDN+RDN1-14, ODPI+DPI1-14, OINV+INV1-14, ORIN+RIN1-14 | Documentos de venta |
| Purchase documents | OPRQ+PRQ1-14, OPQT+PQT1-14, OPOR+POR1-14, OPDN+PDN1-14, OPRR+PRR1-14, ORPD+RPD1-14, ODPO+DPO1-14, OPCH+PCH1-14, ORPC+RPC1-14 | Documentos de compra |
| Drafts | ODRF+DRF1-14 | Borradores |
| Payments | ORCT, RCT1–RCT4, OVPM, VPM1–VPM4 | Pagos |
| Banking | ODSC, DSC1, ODPS (deposits), OCRC, OCRH (credit cards) | Bancos, depósitos, tarjetas |
| Configuration | OHFC (hidden features), OFPR (posting periods), OACP (period categories), OBPL (branches), OHLD+HLD1 (holidays), ORTT (exchange rates) | Configuración |
| Items / inventory / warehouses | OITM, OITW, OIBQ, OBIN, OBTQ, OBBQ, OBTN, OSRQ, OSBQ, OSRN | Artículos e inventario |
| Activities | OCLG, OCLT, OCLS | Actividades |
| Attachments | ATC1 | Anexos |
| Production | ORSC, RSC1–RSC6 (resources), ORST (route stages), OITT, ITT1, ITT2 (BOM), OWOR, WOR1, WOR4 (production orders), ORCJ (resource capacity), ORCM (order recommendations) | Producción |
| Prices | OPLN, ITM1 | Precios |
| Accounting | OJDT, JDT1 | Asientos |
| Electronic transactions | ECM2 | Transacciones electrónicas |

### 4.5.2 Column allowlist

By default all columns of an allowed table are accessible. Restrict them in the same file:

```json
{
  "TableList": [ "ADM1", "ORDR", "CINF" ],
  "ColumnExcludeList": { "ORDR": [ "CreateDate", "UpdateDate" ], "CINF": [ "Algo", "AliasUpd", "TrailDays" ] },
  "ColumnIncludeList": { "ADM1": [ "CurrPeriod", "Street" ] }
}
```

Querying an excluded column (`select Version, Algo from CINF`) → `400`, code **703**, "Column 'Algo' from table 'CINF' not accessible". Table/column names must match the DB letter case.

## 4.6 Supported SQL keywords

| Keyword | Example | Palabra clave (ES) |
|---|---|---|
| `SELECT … FROM … WHERE` | `select ItemCode, ItemName, ItmsGrpCod from oitm where ItemCode > 'i01'` | Básico |
| Alias | `select t1.DocEntry as Col1, t1.DocNum as Col2 from ORDR t1 where t1.DocEntry > 0` | Alias |
| `AND`, `OR`, `NOT`, parentheses | `... where not (t1.DocEntry = 1 or t1.Comments <> '1234') and t1.DocNum = 1` | Lógicos |
| `BETWEEN … AND …` | `select "DocEntry" from ordr where "DocEntry" BETWEEN 1 AND 10` | Rango |
| `ORDER BY` | `... order by t1.DocEntry` | Orden |
| `GROUP BY` (+ `HAVING`) | `select DocStatus, DocType, count(*) as GroupCount from ordr group by DocStatus, DocType having count(*) > 0` | Agrupación |
| `IS [NOT] NULL` | `... where DocEntry is not null and t1.Comments is null` | Nulos |
| Constants | `SELECT 1 as c1, 'string' as c2 FROM OITM` | Constantes |
| `LIKE` | `select CardCode from ordr where CardCode like 'c%'` | Patrón |
| `TOP` | `select top 2 DocStatus, DocType from ordr` | Primeros n |
| `UNION [ALL]` | `select t1.LineNum from rdr1 t1 union all select t1.LineNum from inv1 t1` | Unión |
| `IN` (subquery) | `... where DocEntry in (select t2.DocEntry from rdr1 t2) or DocEntry not in (select t2.DocEntry from inv1 t2)` | IN |
| `EXISTS` | `... where exists(select 1 from rdr1 t2 where t1.DocEntry = t2.DocEntry)` | EXISTS |
| `INNER`, `LEFT [OUTER]`, `RIGHT [OUTER]`, `FULL [OUTER]` join, mixed joins | `select t1.DocEntry, t2.LineNum, t3.CardCode from ordr t1 inner join rdr1 t2 on t1.DocEntry = t2.DocEntry left join ocrd t3 on t1.CardCode = t3.CardCode` | Joins |

## 4.7 Supported SQL functions

| Function | Example | Función (ES) |
|---|---|---|
| `SUM`, `AVG` | `select sum("DocTotal") as sumDocTotal, avg("DocTotal") as avgDocTotal from ordr` | Suma, promedio |
| `MAX`, `MIN` | `select min("DocTotal") as minDocTotal, max("DocTotal") as maxDocTotal from ordr` | Máximo, mínimo |
| `COUNT`, `DISTINCT` | `select count(distinct docEntry) as countDistinct, count(*) as cnt from ordr` | Conteos |
| `ISNULL` / `IFNULL` | `select DocEntry, isnull(comments, 'null comments') as c1, ifnull(Comments, 'null comments') as c2 from ordr` | Nulos |
| `LOWER`, `UPPER` | `SELECT ItemCode, lower(ItemCode) as l, upper(ItemCode) as u FROM [OITM] where lower(ItemCode) = 'i001'` | Mayúsculas/minúsculas |
| `LEFT`, `RIGHT` | `SELECT ItemCode, right(ItemCode, 1) as r, LEFT(ItemCode, 1) as l FROM oitm` | Subcadenas |

Other functions (e.g. `length`) are rejected.

## 4.8 SQL normalization (one SQL for HANA and SQL Server)

| Type | What SL does | Example | Tipo (ES) |
|---|---|---|---|
| Table/column | Fixes identifier case and quoting for the DB (HANA is case-sensitive, SQL Server isn't). Works even if you already quoted with `[]` or `""` | `select itemcode, itemName from oitm` → SQL Server `select [ItemCode], [ItemName] from [OITM]`; HANA `select "ItemCode", "ItemName" from "OITM"` | Tablas/columnas |
| Column alias | Quotes aliases so HANA doesn't upper-case them → same JSON keys on both DBs | `as Col1` → `as [Col1]` / `as "Col1"` (without it HANA returns `COL1`) | Alias |
| Functions | Maps equivalent functions | `ISNULL` → `IFNULL` on HANA; `IFNULL` → `ISNULL` on SQL Server | Funciones |

## 4.9 Parameters

Named parameters with a colon (`:name`), bound to a column:

```http
POST /b1s/v1/SQLQueries
{ "SqlCode": "sql01", "SqlName": "queryOnOrder",
  "SqlText": "select DocEntry, DocTotal, DocDate, comments from ordr where DocTotal > :docTotal" }
→ 201, "ParamList": "docTotal"
```

Execute:

| Way | Request | Forma (ES) |
|---|---|---|
| POST with payload | `POST /b1s/v1/SQLQueries('sql01')/List` `{"ParamList": "docTotal=10.1"}` | Con cuerpo |
| GET with query string | `GET /b1s/v1/SQLQueries('sql01')/List?docTotal=10.1` | Por URL |

Several parameters: `stringParam1='val1'&integerParam2=val2`. Paging links keep the parameters (`...List?docTotal=10.1&$skip=5`).

## 4.10 Errors

| Case | Code | Example message | Caso (ES) |
|---|---|---|---|
| Table not in allowlist | 702 | `Table 'CRD2' not accessible` | Tabla no permitida |
| Column excluded | 703 | `Column 'Algo' from table 'CINF' not accessible` | Columna no permitida |
| Grammar error | 701 | `Invalid SQL syntax: ... Incorrect syntax near 'dsc'.` | Error de sintaxis |
| Unsupported keyword/function | 701 | `... Cannot support this function or expression: 'length'` | No soportado |
| Duplicate alias | 701 | `Multiple name for column or column alias 'min_itemCode' ...` | Alias duplicado |
| Computed column without alias | 701 | Give every computed column a unique alias | Columna calculada sin alias |
| `select *` in main select | 701 | `Cannot support asterisk(*) in select list.` (allowed inside sub-queries, e.g. `exists (select * from rdr1 ...)`) | `select *` no permitido |
| DML (`update`, `insert`, `delete`, `alter`…) | 701 | `mismatched input 'update' expecting {SELECT, '('}` | DML no permitido |
| Parameter injection | 704 | `Parameter error.` | Inyección en parámetros |
| No permission | -6006 (403) | `You are not permitted to perform this action` | Sin permiso |

## 4.11 Permissions

| Need | Where to grant (B1 client as superuser) | Necesidad (ES) |
|---|---|---|
| Run a specific query (`List`) | **Administration > System Initialization > Authorizations > General Authorizations** → subject **Service Layer SQL Query** → the query → *Full Authorization* | Ejecutar una consulta |
| Create/update/delete/read query definitions | Same window → subject **Modify SQL Queries in Service Layer** → *Full Authorization* | Administrar definiciones |

Superusers can do everything. Normal users can read definitions but not create/update/delete them by default. Changes may take ~1 minute (permission cache).

## 4.12 Security

- **SQL injection**: parameter values are tokenized / prepared; e.g. `{"ParamList": "itemCode='i001';truncate table OITM"}` → `400`, code 704 "Parameter error."
- **Change log**: modifications of SQL queries are logged in table **ASQL**.
- **Sensitive data**: use the column allowlist to hide internal columns.

## 4.13 Limitations

- UDO/UDT tables are queryable since **10.0 FP 2102**.
- LOG/history tables (e.g. `AITM`, `ACRD`) can't be queried.
- `SBOCOMMON` / `SBO-COMMON` can't be queried.
- **Data ownership is not applied.**
