# DownPaymentToDraw — Anticipo a utilizar

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `DownPaymentToDraw`
- **Descripción (ES):** Anticipo a utilizar
- **Description (EN):** Down Payment To Draw

- **Properties:** 20

## Properties (20)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 2 | `PostingDate` | Edm.DateTimeOffset | Yes | Posting Date | Fecha de contabilización |
| 3 | `DueDate` | Edm.DateTimeOffset | Yes | Due Date | Fecha de vencimiento |
| 4 | `Name` | Edm.String | Yes | Name | Nombre |
| 5 | `Details` | Edm.String | Yes | Details | Detalles |
| 6 | `AmountToDraw` | Edm.Double | Yes | Amount To Draw | Importe a utilizar |
| 7 | `DownPaymentType` | [DownPaymentTypeEnum](../Enums/DownPaymentTypeEnum.md) | Yes | Down Payment Type | Tipo de anticipo |
| 8 | `AmountToDrawFC` | Edm.Double | Yes | Amount To Draw FC (foreign currency) | Importe a utilizar (ME) |
| 9 | `AmountToDrawSC` | Edm.Double | Yes | Amount To Draw SC (system currency) | Importe a utilizar (moneda del sistema) |
| 10 | `DocInternalID` | Edm.Int32 | Yes | Document Internal ID | ID interno del documento |
| 11 | `RowNum` | Edm.Int32 | Yes | Row Number | Número de línea |
| 12 | `DocNumber` | Edm.Int32 | Yes | Document Number | Número de documento |
| 13 | `Tax` | Edm.Double | Yes | Tax | Impuesto |
| 14 | `TaxFC` | Edm.Double | Yes | Tax FC (foreign currency) | Impuestos (ME) |
| 15 | `TaxSC` | Edm.Double | Yes | Tax SC (system currency) | Impuestos (moneda del sistema) |
| 16 | `GrossAmountToDraw` | Edm.Double | Yes | Gross Amount To Draw | Importe bruto a utilizar |
| 17 | `GrossAmountToDrawFC` | Edm.Double | Yes | Gross Amount To Draw FC (foreign currency) | Importe bruto a utilizar (ME) |
| 18 | `GrossAmountToDrawSC` | Edm.Double | Yes | Gross Amount To Draw SC (system currency) | Importe bruto a utilizar (moneda del sistema) |
| 19 | `IsGrossLine` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Gross Line | Es línea bruta |
| 20 | `DownPaymentsToDrawDetails` | Collection([DownPaymentToDrawDetails](../Tipos-Complejos/DownPaymentToDrawDetails.md)) | Yes | Down Payments To Draw Details | Detalle de anticipos a utilizar |

## Used by (properties)

- [Document](../Entidades/PurchaseQuotations.md).`DownPaymentsToDraw`
