# PMS_SummaryData — Datos de resumen del subproyecto

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `PMS_SummaryData`
- **Descripción (ES):** Datos de resumen del subproyecto
- **Description (EN):** PMS Summary Data

- **Properties:** 34

## Properties (34)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LineID` | Edm.Int32 | Yes | Line ID | ID de línea |
| 2 | `SubprojectBudget` | Edm.Double | Yes | Subproject Budget | Presupuesto del subproyecto |
| 3 | `SumOpenAmountPurchase` | Edm.Double | Yes | Sum Open Amount Purchase | Suma del importe abierto (compras) |
| 4 | `SumInvoicedAmountPurchase` | Edm.Double | Yes | Sum Invoiced Amount Purchase | Suma del importe facturado (compras) |
| 5 | `TotalAmountPurchase` | Edm.Double | Yes | Total Amount Purchase | Importe total (compras) |
| 6 | `TotalVariancePurchase` | Edm.Double | Yes | Total Variance Purchase | Desviación total (compras) |
| 7 | `VariancePerceptionPurchase` | Edm.Double | Yes | Variance Perception Purchase | Desviación de percepción (compras) |
| 8 | `AccumSubprojectBudget` | Edm.Double | Yes | Accum Subproject Budget | Presupuesto acumulado del subproyecto |
| 9 | `AccumOpenAmountPurchase` | Edm.Double | Yes | Accum Open Amount Purchase | Importe abierto acumulado (compras) |
| 10 | `AccumInvoicedAmountPurchase` | Edm.Double | Yes | Accum Invoiced Amount Purchase | Importe facturado acumulado (compras) |
| 11 | `AccumTotalPurchase` | Edm.Double | Yes | Accum Total Purchase | Total acumulado de compras |
| 12 | `AccumTotalVariancePurchase` | Edm.Double | Yes | Accum Total Variance Purchase | Desviación total acumulada (compras) |
| 13 | `AccumVariancePerceptionPurchase` | Edm.Double | Yes | Accum Variance Perception Purchase | Desviación acumulada de percepción (compras) |
| 14 | `PotentialSubprojectAmount` | Edm.Double | Yes | Potential Subproject Amount | Importe potencial del subproyecto |
| 15 | `SumOpenAmountSales` | Edm.Double | Yes | Sum Open Amount Sales | Suma del importe abierto (ventas) |
| 16 | `SumInvoicedAmountSales` | Edm.Double | Yes | Sum Invoiced Amount Sales | Suma del importe facturado (ventas) |
| 17 | `TotalAmountSales` | Edm.Double | Yes | Total Amount Sales | Importe total (ventas) |
| 18 | `TotalVarianceSales` | Edm.Double | Yes | Total Variance Sales | Desviación total (ventas) |
| 19 | `VariancePerceptionSales` | Edm.Double | Yes | Variance Perception Sales | Desviación de percepción (ventas) |
| 20 | `AccumPotentialSubprojectAmount` | Edm.Double | Yes | Accum Potential Subproject Amount | Importe potencial acumulado del subproyecto |
| 21 | `AccumOpenAmountSales` | Edm.Double | Yes | Accum Open Amount Sales | Importe abierto acumulado (ventas) |
| 22 | `AccumInvoicedAmountSales` | Edm.Double | Yes | Accum Invoiced Amount Sales | Importe facturado acumulado (ventas) |
| 23 | `AccumTotalSales` | Edm.Double | Yes | Accum Total Sales | Total acumulado de ventas |
| 24 | `AccumTotalVarianceSales` | Edm.Double | Yes | Accum Total Variance Sales | Desviación total acumulada (ventas) |
| 25 | `AccumVariancePerceptionSales` | Edm.Double | Yes | Accum Variance Perception Sales | Desviación acumulada de percepción (ventas) |
| 26 | `ActualItemComponentCost` | Edm.Double | Yes | Actual Item Component Cost | Costo real de componentes artículo |
| 27 | `ActualResourceComponentCost` | Edm.Double | Yes | Actual Resource Component Cost | Costo real de componentes recurso |
| 28 | `ActualAdditionalCost` | Edm.Double | Yes | Actual Additional Cost | Costo adicional real |
| 29 | `ActualProductCost` | Edm.Double | Yes | Actual Product Cost | Costo real del producto |
| 30 | `ActualByProductCost` | Edm.Double | Yes | Actual By Product Cost | Costo real de subproducto |
| 31 | `TotalVariance` | Edm.Double | Yes | Total Variance | Desviación total |
| 32 | `DueDate` | Edm.DateTimeOffset | Yes | Due Date | Fecha de vencimiento |
| 33 | `ActualClosingDate` | Edm.DateTimeOffset | Yes | Actual Closing Date | Fecha real de cierre |
| 34 | `Overdue` | Edm.Int32 | Yes | Overdue | Vencido |

## Used by (properties)

- [PM_SubprojectDocumentData](PM_SubprojectDocumentData.md).`PMS_SummaryData`
