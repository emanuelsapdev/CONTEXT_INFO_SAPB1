# 3.13–3.15 User-Defined Fields, Tables and Objects (UDF / UDT / UDO)

> Source: *Working with SAP Business One Service Layer* v1.29, sections 3.13–3.15 (paraphrased technical reference).
>
> **Resumen (ES):** crear y administrar campos de usuario (`UserFieldsMD`), tablas de usuario (`UserTablesMD`), claves (`UserKeysMD`) y objetos de usuario (`UserObjectsMD`), y hacer CRUD/cancelar/cerrar sobre ellos.

## Version history

| Version | Capability | Capacidad (ES) |
|---|---|---|
| ≤ 9.1 PL04 | UDFs were dynamic properties of *open types* (`OpenType=true`) | UDF como propiedades dinámicas |
| 9.1 PL03 | CRUD on UDOs | CRUD de UDOs |
| 9.1 PL04 | Manage UDF/UDT/UDO metadata (`UserFieldsMD`, `UserTablesMD`, `UserObjectsMD`) | Gestión de metadatos |
| 9.1 PL05 | UDFs appear in entity definitions; UDTs (no object) accessible; UDF/UDT/UDO in `$metadata` | Aparecen en el metadata |
| 9.2 PL11 | UDO Cancel/Close | Cancelar/cerrar UDO |

All UDFs are prefixed **`U_`**.

## 3.13 User-defined fields

### Managing UDF metadata — entity set `UserFieldsMD` (key: `TableName` + `FieldID`)

DDL on heavily referenced tables can be slow (especially marketing documents).

| Operation | Request | Operación (ES) |
|---|---|---|
| Create | `POST /UserFieldsMD` `{"Name": "u1", "Type": "db_Alpha", "Size": 10, "Description": "udf 1", "SubType": "st_None", "TableName": "OCRD"}` → `201` with `FieldID`, `EditSize`, `Mandatory`, `LinkedTable`, `LinkedUDO`, `ValidValuesMD`, … | Crear |
| Retrieve | `GET /UserFieldsMD(TableName='OCRD', FieldID=0)` | Leer |
| Query | `GET /UserFieldsMD?$filter=Name eq 'u1'` | Consultar |
| Update | `PATCH /UserFieldsMD(TableName='OCRD', FieldID=0)` `{"EditSize": 20, "Description": "Internal Id"}` (field `Type` can't change) | Actualizar |
| Delete | `DELETE /UserFieldsMD(TableName='OCRD', FieldID=0)` | Borrar |

**Automatic propagation:** creating a UDF on a table also creates it on related tables — e.g. on `OCRD` it's also created on `ACRD` (history); on `RDR1` it's created on **all marketing document line tables** (`POR1`, `DLN1`, `INV1`, …) and on `ADO1`. A query by name therefore returns one row per table.

Field types (`BoFieldTypes`): `db_Alpha`, `db_Memo`, `db_Numeric`, `db_Date`, `db_Float`; subtypes (`BoFldSubTypes`): `st_None`, `st_Address`, `st_Phone`, `st_Time`, `st_Rate`, `st_Sum`, `st_Price`, `st_Quantity`, `st_Percentage`, `st_Measurement`, `st_Link`, `st_Image`, `st_Checkbox`.

### CRUD with UDFs

UDF values are regular properties of the entity:

```http
POST /BusinessPartners
{ "CardCode": "bpudf_004", ..., "U_BPSpecRemarks": "First Business Partners with UDF remarks added by Chrome." }

GET /BusinessPartners?$filter=startswith(U_BPSpecRemarks, 'First')
```

## 3.14 User-defined tables (no-object UDTs)

- UDTs of type **"no object"** (`bott_NoObject`) are exposed as simple single-table entities named **`U_<TABLENAME>`**. They can't be used by UDOs.
- In the DB the table is `@<TABLENAME>` (upper case). Use `@MYTBL` when adding UDFs; use `MYTBL` with `UserTablesMD`.

| Step | Request | Paso (ES) |
|---|---|---|
| Create table | `POST /UserTablesMD` `{"TableName": "MYTBL", "TableDescription": "My Table", "TableType": "bott_NoObject"}` | Crear tabla |
| Get table metadata | `GET /UserTablesMD('MYTBL')` | Metadatos de la tabla |
| Add field | `POST /UserFieldsMD` `{"Name": "F1", "Type": "db_Alpha", "Size": 10, "Description": "Customer name", "SubType": "st_None", "TableName": "@MYTBL"}` | Agregar campo |
| Insert row | `POST /U_MYTBL` `{"Code": "C", "Name": "CName", "U_F1": "test data"}` | Insertar |
| Get row (key `Code`) | `GET /U_MYTBL('C')` or `GET /U_MYTBL(Code='C')` | Leer |
| Keys only | `GET /U_MYTBL?$select=Code` | Solo claves |
| Filter | `GET /U_MYTBL?$filter=Name eq 'CName'` | Filtrar |
| Update | `PATCH /U_MYTBL('C')` `{"U_F1": "test data - updated"}` | Actualizar |
| Delete | `DELETE /U_MYTBL('C')` | Borrar |

UDT types (`BoUTBTableType`): `bott_Document`, `bott_DocumentLines`, `bott_MasterData`, `bott_MasterDataLines`, `bott_NoObject`, `bott_NoObjectAutoIncrement`.

## 3.15 User-defined objects

A UDO has **one main UDT** (type *Master Data* or *Document*) and optionally **child UDTs** (*Master Data Rows* or *Document Rows*); each UDT has UDFs. The creation steps are the same as in the B1 client / DI API.

### Example definition: UDO `MyOrder`

| Table | UDT type | UDFs | Tabla (ES) |
|---|---|---|---|
| MyOrder (main) | Document | `CustomerName` (Alphanumeric), `DocTotal` (Units and Totals / Amount) | Principal |
| MyOrderLines (child) | Document Rows | `ItemName` (Alphanumeric), `Price` (Units and Totals / Price), `Quantity` (Units and Totals / Quantity) | Hija |

### 3.15.1 Creating the metadata

```http
POST /UserTablesMD
{ "TableName": "MyOrder", "TableDescription": "My Orders", "TableType": "bott_Document" }
→ 201 { "TableName": "MYORDER", ... }      (DB table: @MYORDER — "@" prefix + upper case)

POST /UserFieldsMD { "Name": "CustomerName", "Type": "db_Alpha", "Size": 10, "Description": "Customer Name", "SubType": "st_None", "TableName": "@MYORDER" }
POST /UserFieldsMD { "Name": "DocTotal", "Type": "db_Float", "Description": "Total Amount", "SubType": "st_Sum", "TableName": "@MYORDER" }

POST /UserTablesMD { "TableName": "MyOrderLines", "TableDescription": "My Order Lines", "TableType": "bott_DocumentLines" }
POST /UserFieldsMD { "Name": "ItemName", "Type": "db_Alpha", "Size": 10, "Description": "Item name", "SubType": "st_None", "TableName": "@MYORDERLINES" }
POST /UserFieldsMD { "Name": "Price", "Type": "db_Float", "Description": "Unit Price", "SubType": "st_Price", "TableName": "@MYORDERLINES" }
POST /UserFieldsMD { "Name": "Quantity", "Type": "db_Float", "Description": "Quantity", "SubType": "st_Quantity", "TableName": "@MYORDERLINES" }

POST /UserObjectsMD
{ "Code": "MyOrder", "Name": "My Orders", "TableName": "MyOrder", "ObjectType": "boud_Document",
  "UserObjectMD_ChildTables": [ { "TableName": "MyOrderLines", "ObjectName": "MyOrderLines" } ] }
```

- The child collection property is named **`<sub-object code>Collection`** (e.g. `MyOrderLinesCollection`). The sub-object code defaults to the UDT name; if that name contains spaces, set a different `ObjectName` at registration (otherwise you'd get `My Order LineCollection`).
- Get the table metadata with `GET /UserTablesMD('MYORDER')`.

### User keys — `UserKeysMD` (key: `TableName` + `KeyIndex`)

```http
POST /UserKeysMD
{ "TableName": "@MYORDER", "KeyIndex": "1", "KeyName": "IX_0", "Unique": "tYES",
  "UserKeysMD_Elements": [ { "ColumnAlias": "CustomerName" } ] }

GET /UserKeysMD(TableName='@MYORDER', KeyIndex=0)
```

### 3.15.2–3.15.5 CRUD on the UDO

| Operation | Request | Operación (ES) |
|---|---|---|
| Create | `POST /MyOrder` `{"U_CustomerName": "c1", "U_DocTotal": 620, "MyOrderLinesCollection": [ {"U_ItemName": "item1", "U_Price": 100, "U_Quantity": 3}, {"U_ItemName": "item2", "U_Price": 80, "U_Quantity": 4} ]}` → `201` with `DocEntry`, `DocNum`, lines with `LineNum` 1, 2 | Crear |
| Get by key (`DocEntry`) | `GET /MyOrder(10)` or `GET /MyOrder(DocEntry=10)` | Leer |
| Keys only | `GET /MyOrder?$select=DocEntry` | Solo claves |
| Filter | `GET /MyOrder?$filter=U_CustomerName eq 'c1' and U_DocTotal gt 1000` | Filtrar |
| Update | `PATCH /MyOrder(10)` `{"U_DocTotal": 700, "MyOrderLines": [ {"LineNum": 2, "U_Quantity": 5} ]}` → `204` (PUT/PATCH/MERGE supported; PATCH = MERGE) | Actualizar |
| Delete | `DELETE /MyOrder(10)` → `204` | Borrar |

Schemas with UDOs: create e.g. `conf/myobj.schema` `{"MyOrder": ["DocEntry", "U_CustomerName"], "MyOrderLines": ["U_ItemName", "U_Quantity"]}` and send `GET /MyOrder(1)` with `B1S-Schema: myobj.schema`.

- **Code** (unique ID) is used in URLs and payloads; **Name** is used in schema files. By default name = code and sub-object name = UDT name; names may contain spaces. The system doesn't prevent duplicate UDO names, so keep them unique yourself.

### 3.15.6 Cancel / Close a UDO

Disabled by default. Enable on the UDO definition, then call the bound actions:

```http
PATCH /UserObjectsMD('MyOrder')
{ "CanClose": "tYES", "CanCancel": "tYES" }

POST /MyOrder(10)/Cancel      → 204
POST /MyOrder(10)/Close       → 204
```

Metadata: `<FunctionImport IsBindable="true" Name="Cancel"><Parameter Name="MYORDERParams" Type="SAPB1.MYORDER"/></FunctionImport>` (same for `Close`).
