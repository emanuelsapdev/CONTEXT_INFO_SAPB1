# SerialNumberDetails — Detalles de números de serie

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `SerialNumberDetails`
- **Descripción (ES):** Detalles de números de serie
- **Entity type:** `SerialNumberDetail` (open type: accepts dynamic/UDF properties)
- **Key:** `DocEntry` (Edm.Int32)
- **DB tables (main / lines):** [OSRN](../../Tablas%20SAP%20B1/OSRN.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 14 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/SerialNumberDetails?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/SerialNumberDetails/$count` | Contar |
| Get by key | `GET /b1s/v2/SerialNumberDetails(1)` | Obtener por clave |
| Create | `POST /b1s/v2/SerialNumberDetails` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/SerialNumberDetails(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/SerialNumberDetails(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/SerialNumberDetails(1)` (only if the B1 object allows removal) | Borrar |

## Properties (14)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` 🔑 | Edm.Int32 | No | Document Entry | DocEntry (clave interna del documento) |
| 2 | `ItemCode` | Edm.String | Yes | Item Code | Código de artículo |
| 3 | `ItemDescription` | Edm.String | Yes | Item Description | Descripción del artículo |
| 4 | `MfrSerialNo` | Edm.String | Yes | Mfr Serial Number | Número de serie del fabricante |
| 5 | `SerialNumber` | Edm.String | Yes | Serial Number | Número de serie |
| 6 | `LotNumber` | Edm.String | Yes | Lot Number | Número de lote |
| 7 | `SystemNumber` | Edm.Int32 | Yes | System Number | Número del sistema |
| 8 | `AdmissionDate` | Edm.DateTimeOffset | Yes | Admission Date | Fecha de admisión |
| 9 | `ManufacturingDate` | Edm.DateTimeOffset | Yes | Manufacturing Date | Fecha de fabricación |
| 10 | `ExpirationDate` | Edm.DateTimeOffset | Yes | Expiration Date | Fecha de vencimiento |
| 11 | `MfrWarrantyStart` | Edm.DateTimeOffset | Yes | Mfr Warranty Start | Inicio de garantía del fabricante |
| 12 | `MFrWarrantyEnd` | Edm.DateTimeOffset | Yes | M Fr Warranty End | Fin de garantía del fabricante |
| 13 | `Location` | Edm.String | Yes | Location | Ubicación |
| 14 | `Details` | Edm.String | Yes | Details | Detalles |

## Navigation properties (1)

Use `GET /b1s/v2/SerialNumberDetails(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `Item` | [Item](../Entidades/Items.md) | [Items](Items.md) | ItemCode → ItemCode | Artículos |
