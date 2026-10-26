# ReportFilter — Filtro de informes de impuestos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ReportFilter`
- **Descripción (ES):** Filtro de informes de impuestos
- **Entity type:** `TaxReportFilter`
- **Key:** `Code` (Edm.Int32)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 35 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ReportFilter?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ReportFilter/$count` | Contar |
| Get by key | `GET /b1s/v2/ReportFilter(1)` | Obtener por clave |
| Create | `POST /b1s/v2/ReportFilter` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ReportFilter(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ReportFilter(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/ReportFilter(1)` (only if the B1 object allows removal) | Borrar |

## Properties (35)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.Int32 | No | Code | Código |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `ReportLayout` | [TaxReportFilterReportLayoutType](../Enums/TaxReportFilterReportLayoutType.md) | Yes | Report Layout | Formato de informe |
| 4 | `FirstPrintedNumber` | Edm.Int32 | Yes | First Printed Number | Primer número impreso |
| 5 | `FromDate` | Edm.DateTimeOffset | Yes | From Date | Fecha desde |
| 6 | `ToDate` | Edm.DateTimeOffset | Yes | To Date | Fecha hasta |
| 7 | `TaxDate` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Tax Date | Fecha del documento (fecha de impuestos) |
| 8 | `RoundAmount` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Round Amount | Importe de redondeo |
| 9 | `DeclarationType` | [TaxReportFilterDeclarationType](../Enums/TaxReportFilterDeclarationType.md) | Yes | Declaration Type | Tipo de declaración |
| 10 | `FilterType` | [TaxReportFilterType](../Enums/TaxReportFilterType.md) | Yes | Filter Type | Tipo de filtro |
| 11 | `ExcludeWT` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Exclude Withholding Tax | Excluir retención |
| 12 | `IncludeCustomers` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Include Customers | Incluir clientes |
| 13 | `IncludeVendors` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Include Vendors | Incluir proveedores |
| 14 | `Period` | [TaxReportFilterPeriod](../Enums/TaxReportFilterPeriod.md) | Yes | Period | Período |
| 15 | `Quarter` | Edm.Int32 | Yes | Quarter | Trimestre |
| 16 | `Year` | Edm.Int32 | Yes | Year | Año |
| 17 | `DocumentType` | [TaxReportFilterApArDocumentType](../Enums/TaxReportFilterApArDocumentType.md) | Yes | Document Type | Tipo de documento |
| 18 | `FirstRegisterNumber` | Edm.Int32 | Yes | First Register Number | Primer número de registro |
| 19 | `IncludeGLAccounts` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Include G/L Accounts | Incluir cuentas de mayor |
| 20 | `AppendixOorPSelection` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Appendix Oor P Selection | Selección de anexo O o P |
| 21 | `OpeningAndClosingBalance` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Opening And Closing Balance | Saldo de apertura y cierre |
| 22 | `FromSeries` | Edm.Int32 | Yes | From Series | Serie desde |
| 23 | `ToSeries` | Edm.Int32 | Yes | To Series | Serie hasta |
| 24 | `Cancellation` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Cancellation | Cancelación |
| 25 | `HideTaxWithoutTransaction` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Hide Tax Without Transaction | Ocultar impuestos sin transacciones |
| 26 | `IncludeSeriesFilter` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Include Series Filter | Incluir filtro de series |
| 27 | `IncludeDocumentType` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Include Document Type | Incluir tipo de documento |
| 28 | `DiplayCreditMemosInSeparateColumn` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Diplay Credit Memos In Separate Column | Mostrar notas de crédito en columna separada |
| 29 | `ShowPaymentsWithDeferredTax` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Show Payments With Deferred Tax | Mostrar pagos con impuesto diferido |
| 30 | `QuarterOrDates` | [TaxReportFilterQuarterOrDates](../Enums/TaxReportFilterQuarterOrDates.md) | Yes | Quarter Or Dates | Trimestre o fechas |
| 31 | `TaxReportGroups` | Collection([TaxReportGroup](../Tipos-Complejos/TaxReportGroup.md)) | Yes | Tax Report Groups | Grupos del informe de impuestos |
| 32 | `TaxReportBusinessPartners` | Collection([TaxReportBusinessPartner](../Tipos-Complejos/TaxReportBusinessPartner.md)) | Yes | Tax Report Business Partners | Socios de negocios del informe de impuestos |
| 33 | `TaxReportDocuments` | Collection([TaxReportDocument](../Tipos-Complejos/TaxReportDocument.md)) | Yes | Tax Report Documents | Documentos del informe de impuestos |
| 34 | `TaxReportSeriesCollection` | Collection([TaxReportSeries](../Tipos-Complejos/TaxReportSeries.md)) | Yes | Tax Report Series Collection | Series del informe de impuestos |
| 35 | `TaxReportAccounts` | Collection([TaxReportAccount](../Tipos-Complejos/TaxReportAccount.md)) | Yes | Tax Report Accounts | Cuentas del informe de impuestos |
