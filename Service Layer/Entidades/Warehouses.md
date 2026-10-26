# Warehouses — Almacenes

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `Warehouses`
- **Descripción (ES):** Almacenes
- **Entity type:** `Warehouse` (open type: accepts dynamic/UDF properties)
- **Key:** `WarehouseCode` (Edm.String)
- **DB tables (main / lines):** [OWHS](../../Tablas%20SAP%20B1/OWHS.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 89 · **Navigation properties:** 18 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/Warehouses?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/Warehouses/$count` | Contar |
| Get by key | `GET /b1s/v2/Warehouses('value')` | Obtener por clave |
| Create | `POST /b1s/v2/Warehouses` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/Warehouses('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/Warehouses('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/Warehouses('value')` (only if the B1 object allows removal) | Borrar |

## Properties (89)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Street` | Edm.String | Yes | Street | Calle |
| 2 | `StockInflationOffsetAccount` | Edm.String | Yes | Stock Inflation Offset Account | Contracuenta de inflación del stock |
| 3 | `ZipCode` | Edm.String | Yes | Zip Code | Código postal |
| 4 | `DecreasingAccount` | Edm.String | Yes | Decreasing Account | Cuenta de disminución |
| 5 | `PurchaseAccount` | Edm.String | Yes | Purchase Account | Cuenta de compras |
| 6 | `EURevenuesAccount` | Edm.String | Yes | EU Revenues Account | Cuenta de ingresos UE |
| 7 | `ReturningAccount` | Edm.String | Yes | Returning Account | Cuenta de devoluciones |
| 8 | `ShippedGoodsAccount` | Edm.String | Yes | Shipped Goods Account | Cuenta de mercancías enviadas |
| 9 | `StockInflationAdjustAccount` | Edm.String | Yes | Stock Inflation Adjust Account | Cuenta de ajuste por inflación del stock |
| 10 | `AllowUseTax` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Allow Use Tax | Permitir impuesto de uso |
| 11 | `CostInflationAccount` | Edm.String | Yes | Cost Inflation Account | Cuenta de inflación de costos |
| 12 | `ForeignExpensesAccount` | Edm.String | Yes | Foreign Expenses Account | Cuenta de gastos del exterior |
| 13 | `EUExpensesAccount` | Edm.String | Yes | EU Expenses Account | Cuenta de gastos UE |
| 14 | `CostInflationOffsetAccount` | Edm.String | Yes | Cost Inflation Offset Account | Contracuenta de inflación de costos |
| 15 | `ExpensesClearingAccount` | Edm.String | Yes | Expenses Clearing Account | Cuenta de compensación de gastos |
| 16 | `PurchaseReturningAccount` | Edm.String | Yes | Purchase Returning Account | Cuenta de devoluciones de compras |
| 17 | `VATInRevenueAccount` | Edm.String | Yes | VAT In Revenue Account | IVA en cuenta de ingresos |
| 18 | `FederalTaxID` | Edm.String | Yes | Federal Tax ID | CUIT / ID fiscal federal |
| 19 | `Location` | Edm.Int32 | Yes | Location | Ubicación |
| 20 | `Block` | Edm.String | Yes | Block | Barrio/bloque |
| 21 | `ExpenseAccount` | Edm.String | Yes | Expense Account | Cuenta de gastos |
| 22 | `DecreaseGLAccount` | Edm.String | Yes | Decrease G/L Account | Cuenta de mayor de disminución |
| 23 | `RevenuesAccount` | Edm.String | Yes | Revenues Account | Cuenta de ingresos |
| 24 | `TaxGroup` | Edm.String | Yes | Tax Group | Grupo de impuestos |
| 25 | `ExemptRevenuesAccount` | Edm.String | Yes | Exempt Revenues Account | Cuenta de ingresos exentos |
| 26 | `PurchaseOffsetAccount` | Edm.String | Yes | Purchase Offset Account | Contracuenta de compras |
| 27 | `CostOfGoodsSold` | Edm.String | Yes | Cost Of Goods Sold | Costo de ventas |
| 28 | `WarehouseCode` 🔑 | Edm.String | No | Warehouse Code | Código de almacén |
| 29 | `State` | Edm.String | Yes | State | Estado/provincia |
| 30 | `City` | Edm.String | Yes | City | Ciudad |
| 31 | `PriceDifferencesAccount` | Edm.String | Yes | Price Differences Account | Cuenta de diferencias de precio |
| 32 | `VarianceAccount` | Edm.String | Yes | Variance Account | Cuenta de desviaciones |
| 33 | `Country` | Edm.String | Yes | Country | País |
| 34 | `IncreaseGLAccount` | Edm.String | Yes | Increase G/L Account | Cuenta de mayor de aumento |
| 35 | `ExchangeRateDifferencesAccount` | Edm.String | Yes | Exchange Rate Differences Account | Cuenta de diferencias de cambio |
| 36 | `WIPMaterialAccount` | Edm.String | Yes | WIP Material Account | Cuenta de materiales WIP |
| 37 | `WarehouseName` | Edm.String | Yes | Warehouse Name | Nombre del almacén |
| 38 | `DropShip` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Drop Ship | Envío directo (drop ship) |
| 39 | `WIPMaterialVarianceAccount` | Edm.String | Yes | WIP Material Variance Account | Cuenta de desviación de materiales WIP |
| 40 | `TransfersAcc` | Edm.String | Yes | Transfers Account | Cuenta de transferencias |
| 41 | `InternalKey` | Edm.Int32 | Yes | Internal Key | Clave interna |
| 42 | `ForeignRevenuesAcc` | Edm.String | Yes | Foreign Revenues Account | Cuenta de ingresos del exterior |
| 43 | `BuildingFloorRoom` | Edm.String | Yes | Building Floor Room | Edificio/piso/oficina |
| 44 | `County` | Edm.String | Yes | County | Condado |
| 45 | `Nettable` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Nettable | Neteable (MRP) |
| 46 | `IncreasingAcc` | Edm.String | Yes | Increasing Account | Cuenta de aumento |
| 47 | `ExpenseOffsetingAct` | Edm.String | Yes | Expense Offseting Act | Contracuenta de gastos |
| 48 | `GoodsClearingAcc` | Edm.String | Yes | Goods Clearing Account | Cuenta de compensación de mercancías |
| 49 | `StockAccount` | Edm.String | Yes | Stock Account | Cuenta de stock |
| 50 | `BusinessPlaceID` | Edm.Int32 | Yes | Business Place ID | ID del lugar de negocios |
| 51 | `PurchaseCreditAcc` | Edm.String | Yes | Purchase Credit Account | Cuenta de haber de compras |
| 52 | `EUPurchaseCreditAcc` | Edm.String | Yes | EU Purchase Credit Account | Cuenta de haber de compras UE |
| 53 | `ForeignPurchaseCreditAcc` | Edm.String | Yes | Foreign Purchase Credit Account | Cuenta de haber de compras del exterior |
| 54 | `SalesCreditAcc` | Edm.String | Yes | Sales Credit Account | Cuenta de haber de ventas |
| 55 | `SalesCreditEUAcc` | Edm.String | Yes | Sales Credit EU Account | Cuenta de haber de ventas UE |
| 56 | `ExemptedCredits` | Edm.String | Yes | Exempted Credits | Créditos exentos |
| 57 | `SalesCreditForeignAcc` | Edm.String | Yes | Sales Credit Foreign Account | Cuenta de haber de ventas del exterior |
| 58 | `NegativeInventoryAdjustmentAccount` | Edm.String | Yes | Negative Inventory Adjustment Account | Cuenta de ajuste de inventario negativo |
| 59 | `WHShipToName` | Edm.String | Yes | Warehouse Ship To Name | Nombre de envío del almacén |
| 60 | `Excisable` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Excisable | Sujeto a impuestos especiales |
| 61 | `WHIncomingCenvatAccount` | Edm.String | Yes | Warehouse Incoming Cenvat Account | Cuenta CENVAT de entrada del almacén |
| 62 | `WHOutgoingCenvatAccount` | Edm.String | Yes | Warehouse Outgoing Cenvat Account | Cuenta CENVAT de salida del almacén |
| 63 | `StockInTransitAccount` | Edm.String | Yes | Stock In Transit Account | Cuenta de stock en tránsito |
| 64 | `WipOffsetProfitAndLossAccount` | Edm.String | Yes | Wip Offset Profit And Loss Account | Contracuenta WIP de pérdidas y ganancias |
| 65 | `InventoryOffsetProfitAndLossAccount` | Edm.String | Yes | Inventory Offset Profit And Loss Account | Contracuenta de inventario de pérdidas y ganancias |
| 66 | `AddressType` | Edm.String | Yes | Address Type | Tipo de dirección |
| 67 | `StreetNo` | Edm.String | Yes | Street Number | Número de calle |
| 68 | `Storekeeper` | Edm.Int32 | Yes | Storekeeper | Almacenero |
| 69 | `Shipper` | Edm.String | Yes | Shipper | Expedidor |
| 70 | `ManageSerialAndBatchNumbers` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Manage Serial And Batch Numbers | Gestionar números de serie y lote |
| 71 | `GlobalLocationNumber` | Edm.String | Yes | Global Location Number | Número de localización global (GLN) |
| 72 | `EnableBinLocations` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enable Bin Locations | Habilitar ubicaciones |
| 73 | `BinLocCodeSeparator` | Edm.String | Yes | Bin Loc Code Separator | Separador de código de ubicación |
| 74 | `DefaultBin` | Edm.Int32 | Yes | Default Bin | Ubicación predeterminada |
| 75 | `DefaultBinEnforced` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Default Bin Enforced | Ubicación predeterminada obligatoria |
| 76 | `AutoAllocOnIssue` | [BoDocWhsAutoIssueMethod](../Enums/BoDocWhsAutoIssueMethod.md) | Yes | Auto Alloc On Issue | Asignación automática en salida |
| 77 | `EnableReceivingBinLocations` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enable Receiving Bin Locations | Habilitar ubicaciones de recepción |
| 78 | `ReceivingBinLocationsBy` | [ReceivingBinLocationsMethodEnum](../Enums/ReceivingBinLocationsMethodEnum.md) | Yes | Receiving Bin Locations By | Ubicaciones de recepción por |
| 79 | `PurchaseBalanceAccount` | Edm.String | Yes | Purchase Balance Account | Cuenta de saldo de compras |
| 80 | `Inactive` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Inactive | Inactivo |
| 81 | `RestrictReceiptToEmptyBinLocation` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Restrict Receipt To Empty Bin Location | Restringir recepción a ubicación vacía |
| 82 | `ReceiveUpToMaxQuantity` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Receive Up To Max Quantity | Recibir hasta cantidad máxima |
| 83 | `AutoAllocOnReceipt` | [AutoAllocOnReceiptMethodEnum](../Enums/AutoAllocOnReceiptMethodEnum.md) | Yes | Auto Alloc On Receipt | Asignación automática en entrada |
| 84 | `ReceiveUpToMaxWeight` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Receive Up To Max Weight | Recibir hasta peso máximo |
| 85 | `ReceiveUpToMethod` | [ReceivingUpToMethodEnum](../Enums/ReceivingUpToMethodEnum.md) | Yes | Receive Up To Method | Método de recepción hasta |
| 86 | `LegalText` | Edm.String | Yes | Legal Text | Texto legal |
| 87 | `AddressName2` | Edm.String | Yes | Address Name 2 | Nombre de dirección 2 |
| 88 | `AddressName3` | Edm.String | Yes | Address Name 3 | Nombre de dirección 3 |
| 89 | `U_B1SYS_COT_code` | Edm.String | Yes | [AR localization] COT code | [Loc. AR] Código COT (Código de Operación de Traslado) |

## Navigation properties (18)

Use `GET /b1s/v2/Warehouses('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `UserDefaultGroups` | Collection([UserDefaultGroup](../Entidades/UserDefaultGroups.md)) | [UserDefaultGroups](UserDefaultGroups.md) |  | Grupos de valores predeterminados de usuario |
| `StockTransfers` | Collection([StockTransfer](../Entidades/StockTransfers.md)) | [StockTransfers](StockTransfers.md) |  | Transferencias de stock |
| `ChartOfAccount` | [ChartOfAccount](../Entidades/ChartOfAccounts.md) | [ChartOfAccounts](ChartOfAccounts.md) | StockInflationOffsetAccount → Code | Plan de cuentas (cuentas de mayor) |
| `WarehouseLocation` | [WarehouseLocation](../Entidades/WarehouseLocations.md) | [WarehouseLocations](WarehouseLocations.md) | Location → Code | Ubicaciones de almacenes |
| `SalesTaxCode` | [SalesTaxCode](../Entidades/SalesTaxCodes.md) | [SalesTaxCodes](SalesTaxCodes.md) | TaxGroup → Code | Códigos del impuesto sobre ventas |
| `Country2` | [Country](../Entidades/Countries.md) | [Countries](Countries.md) | Country → Code | Países/Regiones |
| `County2` | [County](../Entidades/Counties.md) | [Counties](Counties.md) | County → AbsId | Condados |
| `EmployeeInfo` | [EmployeeInfo](../Entidades/EmployeesInfo.md) | [EmployeesInfo](EmployeesInfo.md) | Storekeeper → EmployeeID | Empleados |
| `BusinessPartner` | [BusinessPartner](../Entidades/BusinessPartners.md) | [BusinessPartners](BusinessPartners.md) | Shipper → CardCode | Socio de negocios |
| `BinLocation` | [BinLocation](../Entidades/BinLocations.md) | [BinLocations](BinLocations.md) | DefaultBin → AbsEntry | Ubicaciones (bin locations) |
| `BinLocations` | Collection([BinLocation](../Entidades/BinLocations.md)) | [BinLocations](BinLocations.md) |  | Ubicaciones (bin locations) |
| `GLAccountAdvancedRules` | Collection([GLAccountAdvancedRule](../Entidades/GLAccountAdvancedRules.md)) | [GLAccountAdvancedRules](GLAccountAdvancedRules.md) |  | Reglas avanzadas de cuentas de mayor |
| `InventoryTransferRequests` | Collection([StockTransfer](../Entidades/StockTransfers.md)) | [InventoryTransferRequests](InventoryTransferRequests.md) |  | Solicitudes de transferencia de stock |
| `ResourceCapacities` | Collection([ResourceCapacity](../Entidades/ResourceCapacities.md)) | [ResourceCapacities](ResourceCapacities.md) |  | Capacidades de recursos |
| `StockTransferDrafts` | Collection([StockTransfer](../Entidades/StockTransfers.md)) | [StockTransferDrafts](StockTransferDrafts.md) |  | Borradores de transferencias de stock |
| `ProductionOrders` | Collection([ProductionOrder](../Entidades/ProductionOrders.md)) | [ProductionOrders](ProductionOrders.md) |  | Órdenes de fabricación |
| `BusinessPlaces` | Collection([BusinessPlace](../Entidades/BusinessPlaces.md)) | [BusinessPlaces](BusinessPlaces.md) |  | Lugares de negocios |
| `StockTakings` | Collection([StockTaking](../Entidades/StockTakings.md)) | [StockTakings](StockTakings.md) |  | Toma de inventario |
