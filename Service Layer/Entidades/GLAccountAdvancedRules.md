# GLAccountAdvancedRules — Reglas avanzadas de cuentas de mayor

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `GLAccountAdvancedRules`
- **Descripción (ES):** Reglas avanzadas de cuentas de mayor
- **Entity type:** `GLAccountAdvancedRule`
- **Key:** `AbsoluteEntry` (Edm.Int32)
- **DB tables (main / lines):** [OGAR](../../Tablas%20SAP%20B1/OGAR.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 81 · **Navigation properties:** 9 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/GLAccountAdvancedRules?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/GLAccountAdvancedRules/$count` | Contar |
| Get by key | `GET /b1s/v2/GLAccountAdvancedRules(1)` | Obtener por clave |
| Create | `POST /b1s/v2/GLAccountAdvancedRules` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/GLAccountAdvancedRules(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/GLAccountAdvancedRules(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/GLAccountAdvancedRules(1)` (only if the B1 object allows removal) | Borrar |

## Properties (81)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsoluteEntry` 🔑 | Edm.Int32 | No | Absolute Entry | Entrada absoluta (ID interno) |
| 2 | `Period` | Edm.String | Yes | Period | Período |
| 3 | `BeginningofFinancialYear` | Edm.DateTimeOffset | Yes | Beginningof Financial Year | Inicio del ejercicio |
| 4 | `FinancialYear` | Edm.Int32 | Yes | Financial Year | Ejercicio |
| 5 | `PeriodName` | Edm.String | Yes | Period Name | Nombre del período |
| 6 | `SubPeriodType` | [BoSubPeriodTypeEnum](../Enums/BoSubPeriodTypeEnum.md) | Yes | Sub Period Type | Tipo de subperíodo |
| 7 | `NumberOfPeriods` | Edm.Int32 | Yes | Number Of Periods | Cantidad de períodos |
| 8 | `FromPostingDate` | Edm.DateTimeOffset | Yes | From Posting Date | Fecha de contabilización desde |
| 9 | `ToPostingDate` | Edm.DateTimeOffset | Yes | To Posting Date | Fecha de contabilización hasta |
| 10 | `FromDueDate` | Edm.DateTimeOffset | Yes | From Due Date | Fecha de vencimiento desde |
| 11 | `ToDueDate` | Edm.DateTimeOffset | Yes | To Due Date | Fecha de vencimiento hasta |
| 12 | `FromDocumentDate` | Edm.DateTimeOffset | Yes | From Document Date | Fecha del documento desde |
| 13 | `ToDocumentDate` | Edm.DateTimeOffset | Yes | To Document Date | Fecha del documento hasta |
| 14 | `ItemCode` | Edm.String | Yes | Item Code | Código de artículo |
| 15 | `ItemGroup` | Edm.Int32 | Yes | Item Group | Grupo de artículos |
| 16 | `Warehouse` | Edm.String | Yes | Warehouse | Almacén |
| 17 | `BPGroup` | Edm.Int32 | Yes | Business Partner Group | Grupo de socios de negocios |
| 18 | `FederalTaxID` | Edm.String | Yes | Federal Tax ID | CUIT / ID fiscal federal |
| 19 | `ShipToCountry` | Edm.String | Yes | Ship To Country | País de envío |
| 20 | `ShipToState` | Edm.String | Yes | Ship To State | Estado/provincia de envío |
| 21 | `Description` | Edm.String | Yes | Description | Descripción |
| 22 | `Code` | Edm.String | Yes | Code | Código |
| 23 | `GetGLAccountBy` | [GetGLAccountByEnum](../Enums/GetGLAccountByEnum.md) | Yes | Get G/L Account By | Obtener cuenta de mayor por |
| 24 | `FromDate` | Edm.DateTimeOffset | Yes | From Date | Fecha desde |
| 25 | `ToDate` | Edm.DateTimeOffset | Yes | To Date | Fecha hasta |
| 26 | `ExpensesAccount` | Edm.String | Yes | Expenses Account | Cuenta de gastos |
| 27 | `RevenuesAccount` | Edm.String | Yes | Revenues Account | Cuenta de ingresos |
| 28 | `ExemptIncomeAcc` | Edm.String | Yes | Exempt Income Account | Cuenta de ingresos exentos |
| 29 | `InventoryAccount` | Edm.String | Yes | Inventory Account | Cuenta de inventario |
| 30 | `CostAccount` | Edm.String | Yes | Cost Account | Cuenta de costos |
| 31 | `TransferAccount` | Edm.String | Yes | Transfer Account | Cuenta de transferencia |
| 32 | `VarienceAccount` | Edm.String | Yes | Varience Account | Cuenta de desviaciones |
| 33 | `PriceDifferenceAcc` | Edm.String | Yes | Price Difference Account | Cuenta de diferencias de precio |
| 34 | `NegativeInventoryAdjustmentAccount` | Edm.String | Yes | Negative Inventory Adjustment Account | Cuenta de ajuste de inventario negativo |
| 35 | `DecreasingAccount` | Edm.String | Yes | Decreasing Account | Cuenta de disminución |
| 36 | `IncreasingAccount` | Edm.String | Yes | Increasing Account | Cuenta de aumento |
| 37 | `ReturningAccount` | Edm.String | Yes | Returning Account | Cuenta de devoluciones |
| 38 | `EURevenuesAccount` | Edm.String | Yes | EU Revenues Account | Cuenta de ingresos UE |
| 39 | `EUExpensesAccount` | Edm.String | Yes | EU Expenses Account | Cuenta de gastos UE |
| 40 | `ForeignRevenueAcc` | Edm.String | Yes | Foreign Revenue Account | Cuenta de ingresos del exterior |
| 41 | `ForeignExpensAcc` | Edm.String | Yes | Foreign Expens Account | Cuenta de gastos del exterior |
| 42 | `PurchaseAcct` | Edm.String | Yes | Purchase Account | Cuenta de compras |
| 43 | `PAReturnAcct` | Edm.String | Yes | PA Return Account | Cuenta de devoluciones de compras |
| 44 | `PurchaseOffsetAcct` | Edm.String | Yes | Purchase Offset Account | Contracuenta de compras |
| 45 | `ExchangeRateDifferencesAcct` | Edm.String | Yes | Exchange Rate Differences Account | Cuenta de diferencias de cambio |
| 46 | `GoodsClearingAcct` | Edm.String | Yes | Goods Clearing Account | Cuenta de compensación de mercancías |
| 47 | `GLDecreaseAcct` | Edm.String | Yes | G/L Decrease Account | Cuenta de mayor de disminución |
| 48 | `GLIncreaseAcct` | Edm.String | Yes | G/L Increase Account | Cuenta de mayor de aumento |
| 49 | `WipAccount` | Edm.String | Yes | Wip Account | Cuenta de producción en curso (WIP) |
| 50 | `WipVarianceAccount` | Edm.String | Yes | Wip Variance Account | Cuenta de desviación WIP |
| 51 | `WipOffsetProfitAndLossAccount` | Edm.String | Yes | Wip Offset Profit And Loss Account | Contracuenta WIP de pérdidas y ganancias |
| 52 | `InventoryOffsetProfitAndLossAccount` | Edm.String | Yes | Inventory Offset Profit And Loss Account | Contracuenta de inventario de pérdidas y ganancias |
| 53 | `StockInflationAdjustAccount` | Edm.String | Yes | Stock Inflation Adjust Account | Cuenta de ajuste por inflación del stock |
| 54 | `StockInflationOffsetAccount` | Edm.String | Yes | Stock Inflation Offset Account | Contracuenta de inflación del stock |
| 55 | `CostInflationAccount` | Edm.String | Yes | Cost Inflation Account | Cuenta de inflación de costos |
| 56 | `CostInflationOffsetAccount` | Edm.String | Yes | Cost Inflation Offset Account | Contracuenta de inflación de costos |
| 57 | `ExpenseClearingAct` | Edm.String | Yes | Expense Clearing Act | Cuenta de compensación de gastos |
| 58 | `ExpenseOffsettingAccount` | Edm.String | Yes | Expense Offsetting Account | Contracuenta de gastos |
| 59 | `StockInTransitAccount` | Edm.String | Yes | Stock In Transit Account | Cuenta de stock en tránsito |
| 60 | `ShippedGoodsAccount` | Edm.String | Yes | Shipped Goods Account | Cuenta de mercancías enviadas |
| 61 | `VATInRevenueAccount` | Edm.String | Yes | VAT In Revenue Account | IVA en cuenta de ingresos |
| 62 | `SalesCreditAcc` | Edm.String | Yes | Sales Credit Account | Cuenta de haber de ventas |
| 63 | `PurchaseCreditAcc` | Edm.String | Yes | Purchase Credit Account | Cuenta de haber de compras |
| 64 | `ExemptedCredits` | Edm.String | Yes | Exempted Credits | Créditos exentos |
| 65 | `SalesCreditForeignAcc` | Edm.String | Yes | Sales Credit Foreign Account | Cuenta de haber de ventas del exterior |
| 66 | `ForeignPurchaseCreditAcc` | Edm.String | Yes | Foreign Purchase Credit Account | Cuenta de haber de compras del exterior |
| 67 | `SalesCreditEUAcc` | Edm.String | Yes | Sales Credit EU Account | Cuenta de haber de ventas UE |
| 68 | `EUPurchaseCreditAcc` | Edm.String | Yes | EU Purchase Credit Account | Cuenta de haber de compras UE |
| 69 | `PurchaseBalanceAccount` | Edm.String | Yes | Purchase Balance Account | Cuenta de saldo de compras |
| 70 | `WHIncomingCenvatAccount` | Edm.String | Yes | Warehouse Incoming Cenvat Account | Cuenta CENVAT de entrada del almacén |
| 71 | `WHOutgoingCenvatAccount` | Edm.String | Yes | Warehouse Outgoing Cenvat Account | Cuenta CENVAT de salida del almacén |
| 72 | `IsActive` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Active | Está activo |
| 73 | `BusinessPartnerType` | [BoBusinessPartnerTypes](../Enums/BoBusinessPartnerTypes.md) | Yes | Business Partner Type | Tipo de socio de negocios |
| 74 | `VATGroup` | Edm.String | Yes | VAT Group | Grupo de IVA (indicador de impuesto) |
| 75 | `BPCode` | Edm.String | Yes | Business Partner Code | Código del socio de negocios |
| 76 | `Usage` | Edm.Int32 | Yes | Usage | Uso |
| 77 | `UDF1` | Edm.String | Yes | UDF 1 | UDF 1 |
| 78 | `UDF2` | Edm.String | Yes | UDF 2 | UDF 2 |
| 79 | `UDF3` | Edm.String | Yes | UDF 3 | UDF 3 |
| 80 | `UDF4` | Edm.String | Yes | UDF 4 | UDF 4 |
| 81 | `UDF5` | Edm.String | Yes | UDF 5 | UDF 5 |

## Navigation properties (9)

Use `GET /b1s/v2/GLAccountAdvancedRules(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `Item` | [Item](../Entidades/Items.md) | [Items](Items.md) | ItemCode → ItemCode | Artículos |
| `ItemGroups` | [ItemGroups](../Entidades/ItemGroups.md) | [ItemGroups](ItemGroups.md) | ItemGroup → Number | Grupos de artículos |
| `Warehouse2` | [Warehouse](../Entidades/Warehouses.md) | [Warehouses](Warehouses.md) | Warehouse → WarehouseCode | Almacenes |
| `BusinessPartnerGroup` | [BusinessPartnerGroup](../Entidades/BusinessPartnerGroups.md) | [BusinessPartnerGroups](BusinessPartnerGroups.md) | BPGroup → Code | Grupos de socios de negocios |
| `Country` | [Country](../Entidades/Countries.md) | [Countries](Countries.md) | ShipToCountry → Code | País |
| `ChartOfAccount` | [ChartOfAccount](../Entidades/ChartOfAccounts.md) | [ChartOfAccounts](ChartOfAccounts.md) | ExpensesAccount → Code | Plan de cuentas (cuentas de mayor) |
| `VatGroup` | [VatGroup](../Entidades/VatGroups.md) | [VatGroups](VatGroups.md) | VATGroup → Code | Grupo de IVA (indicador de impuesto) |
| `BusinessPartner` | [BusinessPartner](../Entidades/BusinessPartners.md) | [BusinessPartners](BusinessPartners.md) | BPCode → CardCode | Socio de negocios |
| `NotaFiscalUsage` | [NotaFiscalUsage](../Entidades/NotaFiscalUsage.md) | [NotaFiscalUsage](NotaFiscalUsage.md) | Usage → ID | Uso de Nota Fiscal |
