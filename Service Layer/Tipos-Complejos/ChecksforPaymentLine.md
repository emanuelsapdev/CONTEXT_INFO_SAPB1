# ChecksforPaymentLine — Líneas de cheques para pago

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ChecksforPaymentLine`
- **Descripción (ES):** Líneas de cheques para pago
- **Description (EN):** Checksfor Payment Line
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 8

## Properties (8)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `RowNumber` | Edm.Int32 | Yes | Row Number | Número de línea |
| 2 | `RowDetails` | Edm.String | Yes | Row Details | Detalles de la línea |
| 3 | `RowTotal` | Edm.Double | Yes | Row Total | Total de línea |
| 4 | `RowCurrency` | Edm.String | Yes | Row Currency | Moneda de la línea |
| 5 | `TaxDefinition` | Edm.String | Yes | Tax Definition | Definición de impuestos |
| 6 | `TaxPercent` | Edm.Double | Yes | Tax Percent | Porcentaje de impuesto |
| 7 | `CreditedAccount` | Edm.String | Yes | Credited Account | Cuenta acreditada |
| 8 | `LineTotal` | Edm.Double | Yes | Line Total | Total de línea |

## Used by (properties)

- [ChecksforPayment](../Entidades/ChecksforPayment.md).`ChecksforPaymentLines`
