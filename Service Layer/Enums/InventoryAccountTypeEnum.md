# InventoryAccountTypeEnum — Tipo de cuenta de inventario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `InventoryAccountTypeEnum`
- **Descripción (ES):** Tipo de cuenta de inventario
- **Underlying type:** Edm.Int32
- **Members:** 48

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `iatExpenses` | 0 | Expenses | Gastos |
| `iatRevenues` | 1 | Revenues | Ingresos |
| `iatExemptIncome` | 2 | Exempt Income | Ingresos exentos |
| `iatInventory` | 3 | Inventory | Inventario |
| `iatCost` | 4 | Cost | Costo |
| `iatTransfer` | 5 | Transfer | Transferencia |
| `iatVarience` | 6 | Varience | Desviación |
| `iatPriceDifference` | 7 | Price Difference | Diferencia de precio |
| `iatNegativeInventoryAdjustment` | 8 | Negative Inventory Adjustment | Ajuste de inventario negativo |
| `iatDecreasing` | 9 | Decreasing | Disminución |
| `iatIncreasing` | 10 | Increasing | Aumento |
| `iatReturning` | 11 | Returning | Devoluciones |
| `iatEURevenues` | 12 | EU Revenues | Ingresos UE |
| `iatEUExpenses` | 13 | EU Expenses | Gastos UE |
| `iatForeignRevenue` | 14 | Foreign Revenue | Ingresos del exterior |
| `iatForeignExpens` | 15 | Foreign Expens | Gastos del exterior |
| `iatPurchase` | 16 | Purchase | Compras |
| `iatPAReturn` | 17 | PA Return | Devoluciones de compras |
| `iatPurchaseOffset` | 18 | Purchase Offset | Contracuenta de compras |
| `iatExchangeRateDifferences` | 19 | Exchange Rate Differences | Diferencias de cambio |
| `iatGoodsClearing` | 20 | Goods Clearing | Compensación de mercancías |
| `iatGLDecrease` | 21 | G/L Decrease | Disminución de mayor |
| `iatGLIncrease` | 22 | G/L Increase | Aumento de mayor |
| `iatWip` | 23 | Wip | Producción en curso (WIP) |
| `iatWipVariance` | 24 | Wip Variance | Desviación WIP |
| `iatWipOffsetProfitAndLoss` | 25 | Wip Offset Profit And Loss | Contracuenta WIP de pérdidas y ganancias |
| `iatInventoryOffsetProfitAndLoss` | 26 | Inventory Offset Profit And Loss | Contracuenta de inventario de pérdidas y ganancias |
| `iatStockInflationAdjust` | 27 | Stock Inflation Adjust | Ajuste por inflación del stock |
| `iatStockInflationOffset` | 28 | Stock Inflation Offset | Contracuenta de inflación del stock |
| `iatCostInflation` | 29 | Cost Inflation | Inflación de costos |
| `iatCostInflationOffset` | 30 | Cost Inflation Offset | Contracuenta de inflación de costos |
| `iatExpenseClearing` | 31 | Expense Clearing | Compensación de gastos |
| `iatExpenseOffsetting` | 32 | Expense Offsetting | Contracuenta de gastos |
| `iatStockInTransit` | 33 | Stock In Transit | Stock en tránsito |
| `iatShippedGoods` | 34 | Shipped Goods | Mercancías enviadas |
| `iatVATInRevenue` | 35 | VAT In Revenue | IVA en ingresos |
| `iatSalesCredit` | 36 | Sales Credit | Haber de ventas |
| `iatPurchaseCredit` | 37 | Purchase Credit | Haber de compras |
| `iatExemptedCredits` | 38 | Exempted Credits | Créditos exentos |
| `iatSalesCreditForeign` | 39 | Sales Credit Foreign | Haber de ventas del exterior |
| `iatForeignPurchaseCredit` | 40 | Foreign Purchase Credit | Haber de compras del exterior |
| `iatSalesCreditEU` | 41 | Sales Credit EU | Haber de ventas UE |
| `iatEUPurchaseCredit` | 42 | EU Purchase Credit | Haber de compras UE |
| `iatPurchaseBalance` | 43 | Purchase Balance | Saldo de compras |
| `iatWHIncomingCenvat` | 44 | Warehouse Incoming Cenvat | CENVAT de entrada del almacén |
| `iatWHOutgoingCenvat` | 45 | Warehouse Outgoing Cenvat | CENVAT de salida del almacén |
| `iatFreeOfChargeSales` | 46 | Free Of Charge Sales | Ventas sin cargo |
| `iatFreeOfChargePurchase` | 47 | Free Of Charge Purchase | Compras sin cargo |

## Used by (1 properties)

- [AdvancedGLAccountParams](../Tipos-Complejos/AdvancedGLAccountParams.md).`AccountType`
