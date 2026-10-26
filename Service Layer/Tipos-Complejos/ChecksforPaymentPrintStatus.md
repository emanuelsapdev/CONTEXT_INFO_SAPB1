# ChecksforPaymentPrintStatus — Estado de impresión de cheques para pago

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ChecksforPaymentPrintStatus`
- **Descripción (ES):** Estado de impresión de cheques para pago
- **Description (EN):** Checksfor Payment Print Status
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 5

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 2 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `CheckNumber` | Edm.Int32 | Yes | Check Number | Número de cheque |
| 4 | `PrintStatus` | Edm.String | Yes | Print Status | Estado de impresión |
| 5 | `PrintedBy` | Edm.Int32 | Yes | Printed By | Impreso por |

## Used by (properties)

- [ChecksforPayment](../Entidades/ChecksforPayment.md).`ChecksforPaymentPrintStatus`
