# ItemGroups — Grupos de artículos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ItemGroups`
- **Descripción (ES):** Grupos de artículos
- **Entity type:** `ItemGroups` (open type: accepts dynamic/UDF properties)
- **Key:** `Number` (Edm.Int32)
- **DB tables (main / lines):** [OITB](../../Tablas%20SAP%20B1/OITB.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 64 · **Navigation properties:** 8 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ItemGroups?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ItemGroups/$count` | Contar |
| Get by key | `GET /b1s/v2/ItemGroups(1)` | Obtener por clave |
| Create | `POST /b1s/v2/ItemGroups` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ItemGroups(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ItemGroups(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/ItemGroups(1)` (only if the B1 object allows removal) | Borrar |

## Properties (64)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `PriceDifferencesAccount` | Edm.String | Yes | Price Differences Account | Cuenta de diferencias de precio |
| 2 | `StockInflationAdjustAccount` | Edm.String | Yes | Stock Inflation Adjust Account | Cuenta de ajuste por inflación del stock |
| 3 | `MinimumOrderQuantity` | Edm.Double | Yes | Minimum Order Quantity | Cantidad mínima de pedido |
| 4 | `OrderInterval` | Edm.Int32 | Yes | Order Interval | Intervalo de pedidos |
| 5 | `ExchangeRateDifferencesAccount` | Edm.String | Yes | Exchange Rate Differences Account | Cuenta de diferencias de cambio |
| 6 | `IncreasingAccount` | Edm.String | Yes | Increasing Account | Cuenta de aumento |
| 7 | `StockInflationOffsetAccount` | Edm.String | Yes | Stock Inflation Offset Account | Contracuenta de inflación del stock |
| 8 | `ProcurementMethod` | [BoProcurementMethod](../Enums/BoProcurementMethod.md) | Yes | Procurement Method | Método de aprovisionamiento (comprar/fabricar) |
| 9 | `ComponentWarehouse` | [BoMRPComponentWarehouse](../Enums/BoMRPComponentWarehouse.md) | Yes | Component Warehouse | Almacén de componentes |
| 10 | `PurchaseOffsetAccount` | Edm.String | Yes | Purchase Offset Account | Contracuenta de compras |
| 11 | `InventorySystem` | [BoInventorySystem](../Enums/BoInventorySystem.md) | Yes | Inventory System | Sistema de inventario |
| 12 | `WIPMaterialVarianceAccount` | Edm.String | Yes | WIP Material Variance Account | Cuenta de desviación de materiales WIP |
| 13 | `PlanningSystem` | [BoPlanningSystem](../Enums/BoPlanningSystem.md) | Yes | Planning System | Sistema de planificación (MRP/ninguno) |
| 14 | `PurchaseAccount` | Edm.String | Yes | Purchase Account | Cuenta de compras |
| 15 | `ReturningAccount` | Edm.String | Yes | Returning Account | Cuenta de devoluciones |
| 16 | `CostInflationAccount` | Edm.String | Yes | Cost Inflation Account | Cuenta de inflación de costos |
| 17 | `ExpensesAccount` | Edm.String | Yes | Expenses Account | Cuenta de gastos |
| 18 | `RevenuesAccount` | Edm.String | Yes | Revenues Account | Cuenta de ingresos |
| 19 | `TransfersAccount` | Edm.String | Yes | Transfers Account | Cuenta de transferencias |
| 20 | `LeadTime` | Edm.Int32 | Yes | Lead Time | Tiempo de entrega |
| 21 | `OrderMultiple` | Edm.Double | Yes | Order Multiple | Múltiplo de pedido |
| 22 | `CostInflationOffsetAccount` | Edm.String | Yes | Cost Inflation Offset Account | Contracuenta de inflación de costos |
| 23 | `InventoryAccount` | Edm.String | Yes | Inventory Account | Cuenta de inventario |
| 24 | `DecreaseGLAccount` | Edm.String | Yes | Decrease G/L Account | Cuenta de mayor de disminución |
| 25 | `Number` 🔑 | Edm.Int32 | No | Number | Número |
| 26 | `GoodsClearingAccount` | Edm.String | Yes | Goods Clearing Account | Cuenta de compensación de mercancías |
| 27 | `IncreaseGLAccount` | Edm.String | Yes | Increase G/L Account | Cuenta de mayor de aumento |
| 28 | `ForeignRevenuesAccount` | Edm.String | Yes | Foreign Revenues Account | Cuenta de ingresos del exterior |
| 29 | `Alert` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Alert | Alerta |
| 30 | `WIPMaterialAccount` | Edm.String | Yes | WIP Material Account | Cuenta de materiales WIP |
| 31 | `ShippedGoodsAccount` | Edm.String | Yes | Shipped Goods Account | Cuenta de mercancías enviadas |
| 32 | `ExemptRevenuesAccount` | Edm.String | Yes | Exempt Revenues Account | Cuenta de ingresos exentos |
| 33 | `DecreasingAccount` | Edm.String | Yes | Decreasing Account | Cuenta de disminución |
| 34 | `VATInRevenueAccount` | Edm.String | Yes | VAT In Revenue Account | IVA en cuenta de ingresos |
| 35 | `VarianceAccount` | Edm.String | Yes | Variance Account | Cuenta de desviaciones |
| 36 | `EUExpensesAccount` | Edm.String | Yes | EU Expenses Account | Cuenta de gastos UE |
| 37 | `ForeignExpensesAccount` | Edm.String | Yes | Foreign Expenses Account | Cuenta de gastos del exterior |
| 38 | `CycleCode` | Edm.Int32 | Yes | Cycle Code | Código de ciclo |
| 39 | `CostAccount` | Edm.String | Yes | Cost Account | Cuenta de costos |
| 40 | `EURevenuesAccount` | Edm.String | Yes | EU Revenues Account | Cuenta de ingresos UE |
| 41 | `PAReturnAccount` | Edm.String | Yes | PA Return Account | Cuenta de devoluciones de compras |
| 42 | `GroupName` | Edm.String | Yes | Group Name | Nombre del grupo |
| 43 | `ExpenseClearingAct` | Edm.String | Yes | Expense Clearing Act | Cuenta de compensación de gastos |
| 44 | `PurchaseCreditAcc` | Edm.String | Yes | Purchase Credit Account | Cuenta de haber de compras |
| 45 | `EUPurchaseCreditAcc` | Edm.String | Yes | EU Purchase Credit Account | Cuenta de haber de compras UE |
| 46 | `ForeignPurchaseCreditAcc` | Edm.String | Yes | Foreign Purchase Credit Account | Cuenta de haber de compras del exterior |
| 47 | `SalesCreditAcc` | Edm.String | Yes | Sales Credit Account | Cuenta de haber de ventas |
| 48 | `SalesCreditEUAcc` | Edm.String | Yes | Sales Credit EU Account | Cuenta de haber de ventas UE |
| 49 | `ExemptedCredits` | Edm.String | Yes | Exempted Credits | Créditos exentos |
| 50 | `SalesCreditForeignAcc` | Edm.String | Yes | Sales Credit Foreign Account | Cuenta de haber de ventas del exterior |
| 51 | `ExpenseOffsetAccount` | Edm.String | Yes | Expense Offset Account | Contracuenta de gastos |
| 52 | `NegativeInventoryAdjustmentAccount` | Edm.String | Yes | Negative Inventory Adjustment Account | Cuenta de ajuste de inventario negativo |
| 53 | `WHIncomingCenvatAccount` | Edm.String | Yes | Warehouse Incoming Cenvat Account | Cuenta CENVAT de entrada del almacén |
| 54 | `WHOutgoingCenvatAccount` | Edm.String | Yes | Warehouse Outgoing Cenvat Account | Cuenta CENVAT de salida del almacén |
| 55 | `StockInTransitAccount` | Edm.String | Yes | Stock In Transit Account | Cuenta de stock en tránsito |
| 56 | `WipOffsetProfitAndLossAccount` | Edm.String | Yes | Wip Offset Profit And Loss Account | Contracuenta WIP de pérdidas y ganancias |
| 57 | `InventoryOffsetProfitAndLossAccount` | Edm.String | Yes | Inventory Offset Profit And Loss Account | Contracuenta de inventario de pérdidas y ganancias |
| 58 | `ToleranceDays` | Edm.Int32 | Yes | Tolerance Days | Días de tolerancia |
| 59 | `DefaultUoMGroup` | Edm.Int32 | Yes | Default Uo M Group | Grupo de unidades de medida predeterminado |
| 60 | `DefaultInventoryUoM` | Edm.Int32 | Yes | Default Inventory Uo M | Unidad de medida de inventario predeterminada |
| 61 | `PurchaseBalanceAccount` | Edm.String | Yes | Purchase Balance Account | Cuenta de saldo de compras |
| 62 | `ItemClass` | [ItemClassEnum](../Enums/ItemClassEnum.md) | Yes | Item Class | Clase de artículo (material/servicio) |
| 63 | `RawMaterial` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Raw Material | Materia prima |
| 64 | `ItemGroupsWarehouseInfos` | Collection([ItemGroupsWarehouseInfo](../Tipos-Complejos/ItemGroupsWarehouseInfo.md)) | Yes | Item Groups Warehouse Infos | Información de almacenes del grupo de artículos |

## Navigation properties (8)

Use `GET /b1s/v2/ItemGroups(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `ChartOfAccount` | [ChartOfAccount](../Entidades/ChartOfAccounts.md) | [ChartOfAccounts](ChartOfAccounts.md) | PriceDifferencesAccount → Code | Plan de cuentas (cuentas de mayor) |
| `InventoryCycles` | [InventoryCycles](../Entidades/InventoryCycles.md) | [InventoryCycles](InventoryCycles.md) | OrderInterval → CycleCode | Ciclos de inventario |
| `UnitOfMeasurementGroup` | [UnitOfMeasurementGroup](../Entidades/UnitOfMeasurementGroups.md) | [UnitOfMeasurementGroups](UnitOfMeasurementGroups.md) | DefaultUoMGroup → AbsEntry | Grupos de unidades de medida |
| `UnitOfMeasurement` | [UnitOfMeasurement](../Entidades/UnitOfMeasurements.md) | [UnitOfMeasurements](UnitOfMeasurements.md) | DefaultInventoryUoM → AbsEntry | Unidades de medida |
| `ServiceCalls` | Collection([ServiceCall](../Entidades/ServiceCalls.md)) | [ServiceCalls](ServiceCalls.md) |  | Llamadas de servicio |
| `Items` | Collection([Item](../Entidades/Items.md)) | [Items](Items.md) |  | Artículos |
| `BinLocations` | Collection([BinLocation](../Entidades/BinLocations.md)) | [BinLocations](BinLocations.md) |  | Ubicaciones (bin locations) |
| `GLAccountAdvancedRules` | Collection([GLAccountAdvancedRule](../Entidades/GLAccountAdvancedRules.md)) | [GLAccountAdvancedRules](GLAccountAdvancedRules.md) |  | Reglas avanzadas de cuentas de mayor |
