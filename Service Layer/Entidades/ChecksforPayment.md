# ChecksforPayment — Cheques para pago

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ChecksforPayment`
- **Descripción (ES):** Cheques para pago
- **Entity type:** `ChecksforPayment` (open type: accepts dynamic/UDF properties)
- **Key:** `CheckKey` (Edm.Int32)
- **DB tables (main / lines):** [OCHO](../../Tablas%20SAP%20B1/OCHO.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 40 · **Navigation properties:** 3 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ChecksforPayment?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ChecksforPayment/$count` | Contar |
| Get by key | `GET /b1s/v2/ChecksforPayment(1)` | Obtener por clave |
| Create | `POST /b1s/v2/ChecksforPayment` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ChecksforPayment(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ChecksforPayment(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/ChecksforPayment(1)` (only if the B1 object allows removal) | Borrar |

## Properties (40)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `CheckKey` 🔑 | Edm.Int32 | No | Check Key | Clave del cheque |
| 2 | `CheckNumber` | Edm.Int32 | Yes | Check Number | Número de cheque |
| 3 | `BankCode` | Edm.String | Yes | Bank Code | Código del banco |
| 4 | `Branch` | Edm.String | Yes | Branch | Sucursal |
| 5 | `BankName` | Edm.String | Yes | Bank Name | Nombre del banco |
| 6 | `CheckDate` | Edm.DateTimeOffset | Yes | Check Date | Fecha del cheque |
| 7 | `AccountNumber` | Edm.String | Yes | Account Number | Número de cuenta |
| 8 | `Details` | Edm.String | Yes | Details | Detalles |
| 9 | `JournalEntryReference` | Edm.String | Yes | Journal Entry Reference | Referencia del asiento contable |
| 10 | `PaymentDate` | Edm.DateTimeOffset | Yes | Payment Date | Fecha de pago |
| 11 | `PaymentNo` | Edm.Int32 | Yes | Payment Number | Número de pago |
| 12 | `CheckAmount` | Edm.Double | Yes | Check Amount | Importe del cheque |
| 13 | `Transferable` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Transferable | Transferible |
| 14 | `VendorCode` | Edm.String | Yes | Vendor Code | Código de proveedor |
| 15 | `CheckCurrency` | Edm.String | Yes | Check Currency | Moneda del cheque |
| 16 | `Canceled` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Canceled | Cancelado |
| 17 | `CardOrAccount` | [BoCpCardAcct](../Enums/BoCpCardAcct.md) | Yes | Card Or Account | Socio de negocios o cuenta |
| 18 | `Printed` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Printed | Impreso |
| 19 | `VendorName` | Edm.String | Yes | Vendor Name | Nombre del proveedor |
| 20 | `Signature` | Edm.String | Yes | Signature | Firma |
| 21 | `CustomerAccountCode` | Edm.String | Yes | Customer Account Code | Código de cuenta del cliente |
| 22 | `TransactionNumber` | Edm.Int32 | Yes | Transaction Number | Número de transacción |
| 23 | `Address` | Edm.String | Yes | Address | Dirección |
| 24 | `CreateJournalEntry` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Create Journal Entry | Crear asiento contable |
| 25 | `UpdateDate` | Edm.DateTimeOffset | Yes | Update Date | Fecha de actualización |
| 26 | `CreationDate` | Edm.DateTimeOffset | Yes | Creation Date | Fecha de creación |
| 27 | `TaxTotal` | Edm.Double | Yes | Tax Total | Total de impuestos |
| 28 | `TaxDate` | Edm.DateTimeOffset | Yes | Tax Date | Fecha del documento (fecha de impuestos) |
| 29 | `DeductionRefundAmount` | Edm.Double | Yes | Deduction Refund Amount | Importe de reembolso de deducción |
| 30 | `PrintedBy` | Edm.Int32 | Yes | Printed By | Impreso por |
| 31 | `CountryCode` | Edm.String | Yes | Country Code | Código de país |
| 32 | `TotalinWords` | Edm.String | Yes | Totalin Words | Total en letras |
| 33 | `AddressName` | Edm.String | Yes | Address Name | Nombre de dirección |
| 34 | `ManualCheck` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Manual Check | Cheque manual |
| 35 | `AttachmentEntry` | Edm.Int32 | Yes | Attachment Entry | Entrada de anexo (ID) |
| 36 | `ECheck` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | E Check | Cheque electrónico |
| 37 | `PrintConfirm` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Print Confirm | Confirmación de impresión |
| 38 | `ChecksforPaymentLines` | Collection([ChecksforPaymentLine](../Tipos-Complejos/ChecksforPaymentLine.md)) | Yes | Checksfor Payment Lines | Líneas de cheques para pago |
| 39 | `ChecksforPaymentPrintStatus` | Collection([ChecksforPaymentPrintStatus](../Tipos-Complejos/ChecksforPaymentPrintStatus.md)) | Yes | Checksfor Payment Print Status | Estado de impresión de cheques para pago |
| 40 | `ChecksforPaymentDocumentReferences` | Collection([ChecksforPaymentDocumentReference](../Tipos-Complejos/ChecksforPaymentDocumentReference.md)) | Yes | Checksfor Payment Document References | Referencias de documentos de cheques para pago |

## Navigation properties (3)

Use `GET /b1s/v2/ChecksforPayment(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `JournalEntry` | [JournalEntry](../Entidades/JournalEntries.md) | [JournalEntries](JournalEntries.md) | TransactionNumber → JdtNum | Asientos contables |
| `Country` | [Country](../Entidades/Countries.md) | [Countries](Countries.md) | CountryCode → Code | País |
| `Attachments2` | [Attachments2](../Entidades/Attachments2.md) | [Attachments2](Attachments2.md) | AttachmentEntry → AbsoluteEntry | Anexos |
