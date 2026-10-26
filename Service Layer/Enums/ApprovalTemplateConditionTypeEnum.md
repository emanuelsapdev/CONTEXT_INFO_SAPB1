# ApprovalTemplateConditionTypeEnum — Tipo de condición del modelo de autorización

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `ApprovalTemplateConditionTypeEnum`
- **Descripción (ES):** Tipo de condición del modelo de autorización
- **Underlying type:** Edm.Int32
- **Members:** 13

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `atctUndefined` | 0 | Undefined | Indefinido |
| `atctDeviationFromCreditLine` | 1 | Deviation From Credit Line | Desviación del límite de crédito |
| `atctDeviationFromObligo` | 2 | Deviation From Obligo | Desviación del límite de compromiso |
| `atctGrossProfitPercent` | 3 | Gross Profit Percent | Porcentaje de margen bruto |
| `atctDiscountPercent` | 4 | Discount Percent | Porcentaje de descuento |
| `atctDeviationFromBudget` | 5 | Deviation From Budget | Desviación del presupuesto |
| `atctTotalDocument` | 6 | Total Document | Total del documento |
| `atctItemCode` | 7 | Item Code | Código de artículo |
| `atctTotalLine` | 8 | Total Line | Total de línea |
| `atctCountedQuantity` | 9 | Counted Quantity | Cantidad contada |
| `atctQuantity` | 10 | Quantity | Cantidad |
| `atctVariance` | 11 | Variance | Desviación |
| `atctVariancePercent` | 12 | Variance Percent | Porcentaje de desviación |

## Used by (1 properties)

- [ApprovalTemplateTerm](../Tipos-Complejos/ApprovalTemplateTerm.md).`ConditionType`
