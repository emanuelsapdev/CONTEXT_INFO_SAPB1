# ItemWarehouseInfo — Datos del artículo por almacén

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ItemWarehouseInfo`
- **Descripción (ES):** Datos del artículo por almacén
- **Description (EN):** Item Warehouse Information
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 65

## Properties (65)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `MinimalStock` | Edm.Double | Yes | Minimal Stock | Stock mínimo |
| 2 | `MaximalStock` | Edm.Double | Yes | Maximal Stock | Stock máximo |
| 3 | `MinimalOrder` | Edm.Double | Yes | Minimal Order | Pedido mínimo |
| 4 | `StandardAveragePrice` | Edm.Double | Yes | Standard Average Price | Precio promedio estándar |
| 5 | `Locked` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Locked | Bloqueado |
| 6 | `InventoryAccount` | Edm.String | Yes | Inventory Account | Cuenta de inventario |
| 7 | `CostAccount` | Edm.String | Yes | Cost Account | Cuenta de costos |
| 8 | `TransferAccount` | Edm.String | Yes | Transfer Account | Cuenta de transferencia |
| 9 | `RevenuesAccount` | Edm.String | Yes | Revenues Account | Cuenta de ingresos |
| 10 | `VarienceAccount` | Edm.String | Yes | Varience Account | Cuenta de desviaciones |
| 11 | `DecreasingAccount` | Edm.String | Yes | Decreasing Account | Cuenta de disminución |
| 12 | `IncreasingAccount` | Edm.String | Yes | Increasing Account | Cuenta de aumento |
| 13 | `ReturningAccount` | Edm.String | Yes | Returning Account | Cuenta de devoluciones |
| 14 | `ExpensesAccount` | Edm.String | Yes | Expenses Account | Cuenta de gastos |
| 15 | `EURevenuesAccount` | Edm.String | Yes | EU Revenues Account | Cuenta de ingresos UE |
| 16 | `EUExpensesAccount` | Edm.String | Yes | EU Expenses Account | Cuenta de gastos UE |
| 17 | `ForeignRevenueAcc` | Edm.String | Yes | Foreign Revenue Account | Cuenta de ingresos del exterior |
| 18 | `ForeignExpensAcc` | Edm.String | Yes | Foreign Expens Account | Cuenta de gastos del exterior |
| 19 | `ExemptIncomeAcc` | Edm.String | Yes | Exempt Income Account | Cuenta de ingresos exentos |
| 20 | `PriceDifferenceAcc` | Edm.String | Yes | Price Difference Account | Cuenta de diferencias de precio |
| 21 | `WarehouseCode` | Edm.String | Yes | Warehouse Code | Código de almacén |
| 22 | `InStock` | Edm.Double | Yes | In Stock | En stock |
| 23 | `Committed` | Edm.Double | Yes | Committed | Comprometido |
| 24 | `Ordered` | Edm.Double | Yes | Ordered | Pedido (cantidad solicitada a proveedores) |
| 25 | `CountedQuantity` | Edm.Double | Yes | Counted Quantity | Cantidad contada |
| 26 | `WasCounted` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Was Counted | Fue contado |
| 27 | `UserSignature` | Edm.Int32 | Yes | User Signature | Firma del usuario |
| 28 | `Counted` | Edm.Double | Yes | Counted | Contado |
| 29 | `ExpenseClearingAct` | Edm.String | Yes | Expense Clearing Act | Cuenta de compensación de gastos |
| 30 | `PurchaseCreditAcc` | Edm.String | Yes | Purchase Credit Account | Cuenta de haber de compras |
| 31 | `EUPurchaseCreditAcc` | Edm.String | Yes | EU Purchase Credit Account | Cuenta de haber de compras UE |
| 32 | `ForeignPurchaseCreditAcc` | Edm.String | Yes | Foreign Purchase Credit Account | Cuenta de haber de compras del exterior |
| 33 | `SalesCreditAcc` | Edm.String | Yes | Sales Credit Account | Cuenta de haber de ventas |
| 34 | `SalesCreditEUAcc` | Edm.String | Yes | Sales Credit EU Account | Cuenta de haber de ventas UE |
| 35 | `ExemptedCredits` | Edm.String | Yes | Exempted Credits | Créditos exentos |
| 36 | `SalesCreditForeignAcc` | Edm.String | Yes | Sales Credit Foreign Account | Cuenta de haber de ventas del exterior |
| 37 | `ExpenseOffsettingAccount` | Edm.String | Yes | Expense Offsetting Account | Contracuenta de gastos |
| 38 | `WipAccount` | Edm.String | Yes | Wip Account | Cuenta de producción en curso (WIP) |
| 39 | `ExchangeRateDifferencesAcct` | Edm.String | Yes | Exchange Rate Differences Account | Cuenta de diferencias de cambio |
| 40 | `GoodsClearingAcct` | Edm.String | Yes | Goods Clearing Account | Cuenta de compensación de mercancías |
| 41 | `NegativeInventoryAdjustmentAccount` | Edm.String | Yes | Negative Inventory Adjustment Account | Cuenta de ajuste de inventario negativo |
| 42 | `CostInflationOffsetAccount` | Edm.String | Yes | Cost Inflation Offset Account | Contracuenta de inflación de costos |
| 43 | `GLDecreaseAcct` | Edm.String | Yes | G/L Decrease Account | Cuenta de mayor de disminución |
| 44 | `GLIncreaseAcct` | Edm.String | Yes | G/L Increase Account | Cuenta de mayor de aumento |
| 45 | `PAReturnAcct` | Edm.String | Yes | PA Return Account | Cuenta de devoluciones de compras |
| 46 | `PurchaseAcct` | Edm.String | Yes | Purchase Account | Cuenta de compras |
| 47 | `PurchaseOffsetAcct` | Edm.String | Yes | Purchase Offset Account | Contracuenta de compras |
| 48 | `ShippedGoodsAccount` | Edm.String | Yes | Shipped Goods Account | Cuenta de mercancías enviadas |
| 49 | `StockInflationOffsetAccount` | Edm.String | Yes | Stock Inflation Offset Account | Contracuenta de inflación del stock |
| 50 | `StockInflationAdjustAccount` | Edm.String | Yes | Stock Inflation Adjust Account | Cuenta de ajuste por inflación del stock |
| 51 | `VATInRevenueAccount` | Edm.String | Yes | VAT In Revenue Account | IVA en cuenta de ingresos |
| 52 | `WipVarianceAccount` | Edm.String | Yes | Wip Variance Account | Cuenta de desviación WIP |
| 53 | `CostInflationAccount` | Edm.String | Yes | Cost Inflation Account | Cuenta de inflación de costos |
| 54 | `WHIncomingCenvatAccount` | Edm.String | Yes | Warehouse Incoming Cenvat Account | Cuenta CENVAT de entrada del almacén |
| 55 | `WHOutgoingCenvatAccount` | Edm.String | Yes | Warehouse Outgoing Cenvat Account | Cuenta CENVAT de salida del almacén |
| 56 | `StockInTransitAccount` | Edm.String | Yes | Stock In Transit Account | Cuenta de stock en tránsito |
| 57 | `WipOffsetProfitAndLossAccount` | Edm.String | Yes | Wip Offset Profit And Loss Account | Contracuenta WIP de pérdidas y ganancias |
| 58 | `InventoryOffsetProfitAndLossAccount` | Edm.String | Yes | Inventory Offset Profit And Loss Account | Contracuenta de inventario de pérdidas y ganancias |
| 59 | `DefaultBin` | Edm.Int32 | Yes | Default Bin | Ubicación predeterminada |
| 60 | `DefaultBinEnforced` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Default Bin Enforced | Ubicación predeterminada obligatoria |
| 61 | `PurchaseBalanceAccount` | Edm.String | Yes | Purchase Balance Account | Cuenta de saldo de compras |
| 62 | `ItemCode` | Edm.String | Yes | Item Code | Código de artículo |
| 63 | `IndEscala` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Ind Escala | Indicador de escala relevante (Brasil) |
| 64 | `CNJPMan` | Edm.String | Yes | CNJP Man | CNPJ del fabricante |
| 65 | `ItemCycleCounts` | Collection([ItemCycleCount](../Tipos-Complejos/ItemCycleCount.md)) | Yes | Item Cycle Counts | Recuentos cíclicos del artículo |

## Used by (properties)

- [Item](../Entidades/Items.md).`ItemWarehouseInfoCollection`
