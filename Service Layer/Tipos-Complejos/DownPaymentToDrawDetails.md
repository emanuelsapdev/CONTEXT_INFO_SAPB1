# DownPaymentToDrawDetails — Detalle de anticipo a utilizar

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `DownPaymentToDrawDetails`
- **Descripción (ES):** Detalle de anticipo a utilizar
- **Description (EN):** Down Payment To Draw Details

- **Properties:** 18

## Properties (18)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocInternalID` | Edm.Int32 | Yes | Document Internal ID | ID interno del documento |
| 2 | `RowNum` | Edm.Int32 | Yes | Row Number | Número de línea |
| 3 | `SeqNum` | Edm.Int32 | Yes | Seq Number | Número de secuencia |
| 4 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 5 | `VatGroupCode` | Edm.String | Yes | Vat Group Code | Código de grupo de IVA |
| 6 | `VatPercent` | Edm.Double | Yes | Vat Percent | Porcentaje de IVA |
| 7 | `AmountToDraw` | Edm.Double | Yes | Amount To Draw | Importe a utilizar |
| 8 | `AmountToDrawFC` | Edm.Double | Yes | Amount To Draw FC (foreign currency) | Importe a utilizar (ME) |
| 9 | `AmountToDrawSC` | Edm.Double | Yes | Amount To Draw SC (system currency) | Importe a utilizar (moneda del sistema) |
| 10 | `Tax` | Edm.Double | Yes | Tax | Impuesto |
| 11 | `TaxFC` | Edm.Double | Yes | Tax FC (foreign currency) | Impuestos (ME) |
| 12 | `TaxSC` | Edm.Double | Yes | Tax SC (system currency) | Impuestos (moneda del sistema) |
| 13 | `IsGrossLine` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Gross Line | Es línea bruta |
| 14 | `GrossAmountToDraw` | Edm.Double | Yes | Gross Amount To Draw | Importe bruto a utilizar |
| 15 | `GrossAmountToDrawFC` | Edm.Double | Yes | Gross Amount To Draw FC (foreign currency) | Importe bruto a utilizar (ME) |
| 16 | `GrossAmountToDrawSC` | Edm.Double | Yes | Gross Amount To Draw SC (system currency) | Importe bruto a utilizar (moneda del sistema) |
| 17 | `LineType` | [LineTypeEnum](../Enums/LineTypeEnum.md) | Yes | Line Type | Tipo de línea |
| 18 | `TaxAdjust` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Tax Adjust | Ajuste de impuestos |

## Used by (properties)

- [DownPaymentToDraw](DownPaymentToDraw.md).`DownPaymentsToDrawDetails`
