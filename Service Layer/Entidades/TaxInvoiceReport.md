# TaxInvoiceReport — Informe de facturas de impuestos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `TaxInvoiceReport`
- **Descripción (ES):** Informe de facturas de impuestos
- **Entity type:** `TaxInvoiceReport`
- **Key:** `TaxInvoiceReportNumber` (Edm.String)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 16 · **Navigation properties:** 1 · **Bound actions:** 1

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/TaxInvoiceReport?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/TaxInvoiceReport/$count` | Contar |
| Get by key | `GET /b1s/v2/TaxInvoiceReport('value')` | Obtener por clave |
| Create | `POST /b1s/v2/TaxInvoiceReport` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/TaxInvoiceReport('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/TaxInvoiceReport('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/TaxInvoiceReport('value')` (only if the B1 object allows removal) | Borrar |
| Action `CancelTaxInvoiceReport` | `POST /b1s/v2/TaxInvoiceReport('value')/CancelTaxInvoiceReport` | Cancelar informe de facturas de impuestos |

## Properties (16)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `NTSApproval` | [TaxInvoiceReportNTSApprovedEnum](../Enums/TaxInvoiceReportNTSApprovedEnum.md) | Yes | NTS Approval | Aprobación NTS (Corea) |
| 2 | `ETaxWebSite` | Edm.Int32 | Yes | E Tax Web Site | Sitio web de impuestos electrónicos |
| 3 | `ETaxNo` | Edm.String | Yes | E Tax Number | Número de impuesto electrónico |
| 4 | `NTSApprovalNo` | Edm.String | Yes | NTS Approval Number | N.º de aprobación NTS |
| 5 | `OriginalNTSApprovalNo` | Edm.String | Yes | Original NTS Approval Number | N.º de aprobación NTS original |
| 6 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 7 | `TaxInvoiceReportNumber` 🔑 | Edm.String | No | Tax Invoice Report Number | Número del informe de facturas de impuestos |
| 8 | `Date` | Edm.DateTimeOffset | Yes | Date | Fecha |
| 9 | `BusinessPlace` | Edm.Int32 | Yes | Business Place | Lugar de negocios |
| 10 | `BPCode` | Edm.String | Yes | Business Partner Code | Código del socio de negocios |
| 11 | `BPName` | Edm.String | Yes | Business Partner Name | Nombre del socio de negocios |
| 12 | `BaseAmount` | Edm.Double | Yes | Base Amount | Importe base |
| 13 | `TaxAmount` | Edm.Double | Yes | Tax Amount | Importe de impuestos |
| 14 | `Canceled` | Edm.String | Yes | Canceled | Cancelado |
| 15 | `ReportType` | Edm.Int32 | Yes | Report Type | Tipo de informe |
| 16 | `TaxInvoiceReportLineCollection` | Collection([TaxInvoiceReportLine](../Tipos-Complejos/TaxInvoiceReportLine.md)) | Yes | Tax Invoice Report Line Collection | Líneas del informe de facturas de impuestos |

## Navigation properties (1)

Use `GET /b1s/v2/TaxInvoiceReport('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `TaxWebSite` | [TaxWebSite](../Entidades/TaxWebSites.md) | [TaxWebSites](TaxWebSites.md) | ETaxWebSite → AbsEntry | Sitios web de impuestos |

## Bound actions (1)

### CancelTaxInvoiceReport

- **Descripción (ES):** Cancelar informe de facturas de impuestos
- **Request:** `POST /b1s/v2/TaxInvoiceReport('value')/CancelTaxInvoiceReport`

