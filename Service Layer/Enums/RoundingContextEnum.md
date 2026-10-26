# RoundingContextEnum — Contexto de redondeo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `RoundingContextEnum`
- **Descripción (ES):** Contexto de redondeo
- **Underlying type:** Edm.Int32
- **Members:** 19

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `rcSum` | 7 | Sum | Importe |
| `rcPrice` | 8 | Price | Precio |
| `rcRate` | 9 | Rate | Tipo de cambio |
| `rcQuantity` | 10 | Quantity | Cantidad |
| `rcMeasure` | 11 | Measure | Unidad de medida |
| `rcPercent` | 12 | Percent | Porcentaje |
| `rcTax` | 13 | Tax | Impuesto |
| `rcTaxPerGroup` | 14 | Tax Per Group | Impuesto por grupo |
| `rcBudgetSum` | 16 | Budget Sum | Importe de presupuesto |
| `rcPriceListSum` | 17 | Price List Sum | Importe de lista de precios |
| `rcRealAmountInPayment` | 18 | Real Amount In Payment | Importe real en el pago |
| `rcStockSumRoundUp` | 19 | Stock Sum Round Up | Importe de stock redondeado hacia arriba |
| `rcDocHeaderTotal` | 20 | Document Header Total | Total de cabecera del documento |
| `rcVatReportAmount` | 21 | Vat Report Amount | Importe del informe de IVA |
| `rcLineGrossTotal` | 22 | Line Gross Total | Total bruto de línea |
| `rcExpenseTotal` | 23 | Expense Total | Total de gastos |
| `rcWTax` | 24 | W Tax | Retención |
| `rcBASCode` | 25 | BAS Code | Código BAS |
| `rcTaxForPrice` | 26 | Tax For Price | Impuesto para precio |

## Used by (1 properties)

- [DecimalData](../Tipos-Complejos/DecimalData.md).`Context`
