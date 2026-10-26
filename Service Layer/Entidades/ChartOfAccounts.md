# ChartOfAccounts — Plan de cuentas (cuentas de mayor)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ChartOfAccounts`
- **Descripción (ES):** Plan de cuentas (cuentas de mayor)
- **Entity type:** `ChartOfAccount` (open type: accepts dynamic/UDF properties)
- **Key:** `Code` (Edm.String)
- **DB tables (main / lines):** [OACT](../../Tablas%20SAP%20B1/OACT.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 78 · **Navigation properties:** 54 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ChartOfAccounts?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ChartOfAccounts/$count` | Contar |
| Get by key | `GET /b1s/v2/ChartOfAccounts('value')` | Obtener por clave |
| Create | `POST /b1s/v2/ChartOfAccounts` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ChartOfAccounts('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ChartOfAccounts('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/ChartOfAccounts('value')` (only if the B1 object allows removal) | Borrar |

## Properties (78)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.String | No | Code | Código |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `Balance` | Edm.Double | Yes | Balance | Saldo |
| 4 | `CashAccount` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Cash Account | Cuenta de caja |
| 5 | `BudgetAccount` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Budget Account | Cuenta de presupuesto |
| 6 | `ActiveAccount` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Active Account | Cuenta activa |
| 7 | `PrimaryAccount` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Primary Account | Cuenta principal |
| 8 | `AccountLevel` | Edm.Int32 | Yes | Account Level | Nivel de cuenta |
| 9 | `DataExportCode` | Edm.String | Yes | Data Export Code | Código de exportación de datos |
| 10 | `FatherAccountKey` | Edm.String | Yes | Father Account Key | Cuenta padre |
| 11 | `ExternalCode` | Edm.String | Yes | External Code | Código externo |
| 12 | `RateConversion` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Rate Conversion | Conversión de tipo de cambio |
| 13 | `TaxLiableAccount` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Tax Liable Account | Cuenta sujeta a impuestos |
| 14 | `TaxExemptAccount` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Tax Exempt Account | Cuenta exenta de impuestos |
| 15 | `ExternalReconNo` | Edm.Int32 | Yes | External Recon Number | Número de conciliación externa |
| 16 | `InternalReconNo` | Edm.Int32 | Yes | Internal Recon Number | Número de conciliación interna |
| 17 | `AccountType` | [BoAccountTypes](../Enums/BoAccountTypes.md) | Yes | Account Type | Tipo de cuenta |
| 18 | `AcctCurrency` | Edm.String | Yes | Account Currency | Moneda de la cuenta |
| 19 | `Balance_syscurr` | Edm.Double | Yes | Balance syscurr | Saldo (moneda del sistema) |
| 20 | `Balance_FrgnCurr` | Edm.Double | Yes | Balance Frgn Currency | Saldo (moneda extranjera) |
| 21 | `Protected` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Protected | Protegido |
| 22 | `ReconciledAccount` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Reconciled Account | Cuenta conciliada |
| 23 | `LiableForAdvances` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Liable For Advances | Sujeto a anticipos |
| 24 | `ForeignName` | Edm.String | Yes | Foreign Name | Nombre extranjero |
| 25 | `Details` | Edm.String | Yes | Details | Detalles |
| 26 | `ProjectCode` | Edm.String | Yes | Project Code | Código de proyecto |
| 27 | `RevaluationCoordinated` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Revaluation Coordinated | Revalorización coordinada |
| 28 | `LockManualTransaction` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Lock Manual Transaction | Bloquear transacción manual |
| 29 | `FormatCode` | Edm.String | Yes | Format Code | Código de formato |
| 30 | `AllowChangeVatGroup` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Allow Change Vat Group | Permitir cambiar grupo de IVA |
| 31 | `DefaultVatGroup` | Edm.String | Yes | Default Vat Group | Grupo de IVA predeterminado |
| 32 | `Category` | Edm.Int32 | Yes | Category | Categoría |
| 33 | `TransactionCode` | Edm.String | Yes | Transaction Code | Código de transacción |
| 34 | `LoadingType` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Loading Type | Tipo de carga |
| 35 | `LoadingFactorCode` | Edm.String | Yes | Loading Factor Code | Código de factor de carga |
| 36 | `LoadingFactorCode2` | Edm.String | Yes | Loading Factor Code 2 | Código de factor de carga 2 |
| 37 | `LoadingFactorCode3` | Edm.String | Yes | Loading Factor Code 3 | Código de factor de carga 3 |
| 38 | `LoadingFactorCode4` | Edm.String | Yes | Loading Factor Code 4 | Código de factor de carga 4 |
| 39 | `LoadingFactorCode5` | Edm.String | Yes | Loading Factor Code 5 | Código de factor de carga 5 |
| 40 | `PlanningLevel` | Edm.String | Yes | Planning Level | Nivel de planificación |
| 41 | `DatevAccount` | Edm.String | Yes | Datev Account | Cuenta DATEV |
| 42 | `DatevAutoAccount` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Datev Auto Account | Cuenta automática DATEV |
| 43 | `DatevFirstDataEntry` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Datev First Data Entry | Primera entrada de datos DATEV |
| 44 | `AllowMultipleLinking` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Allow Multiple Linking | Permitir vinculación múltiple |
| 45 | `ProjectRelevant` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Project Relevant | Relevante para proyecto |
| 46 | `DistributionRuleRelevant` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Distribution Rule Relevant | Relevante para norma de reparto |
| 47 | `DistributionRule2Relevant` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Distribution Rule 2 Relevant | Relevante para norma de reparto 2 |
| 48 | `DistributionRule3Relevant` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Distribution Rule 3 Relevant | Relevante para norma de reparto 3 |
| 49 | `DistributionRule4Relevant` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Distribution Rule 4 Relevant | Relevante para norma de reparto 4 |
| 50 | `DistributionRule5Relevant` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Distribution Rule 5 Relevant | Relevante para norma de reparto 5 |
| 51 | `BPLID` | Edm.Int32 | Yes | BPLID | ID de sucursal |
| 52 | `BPLName` | Edm.String | Yes | Branch Name | Nombre de la sucursal |
| 53 | `VATRegNum` | Edm.String | Yes | VAT Reg Number | Número de registro de IVA |
| 54 | `AccountPurposeCode` | [SPEDContabilAccountPurposeCode](../Enums/SPEDContabilAccountPurposeCode.md) | Yes | Account Purpose Code | Código de finalidad de la cuenta |
| 55 | `ReferentialAccountCode` | Edm.String | Yes | Referential Account Code | Código de cuenta referencial |
| 56 | `ValidFor` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Valid For | Válido para |
| 57 | `ValidFrom` | Edm.DateTimeOffset | Yes | Valid From | Válido desde |
| 58 | `ValidTo` | Edm.DateTimeOffset | Yes | Valid To | Válido hasta |
| 59 | `ValidRemarks` | Edm.String | Yes | Valid Remarks | Comentarios de validez |
| 60 | `FrozenFor` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Frozen For | Congelado para |
| 61 | `FrozenFrom` | Edm.DateTimeOffset | Yes | Frozen From | Congelado desde |
| 62 | `FrozenTo` | Edm.DateTimeOffset | Yes | Frozen To | Congelado hasta |
| 63 | `FrozenRemarks` | Edm.String | Yes | Frozen Remarks | Comentarios de congelación |
| 64 | `BlockManualPosting` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Block Manual Posting | Bloquear contabilización manual |
| 65 | `CashFlowRelevant` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Cash Flow Relevant | Relevante para flujo de caja |
| 66 | `PCN874ReportRelevant` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | PCN 874 Report Relevant | Relevante para informe PCN874 (Israel) |
| 67 | `PrimaryClosingAccount` | Edm.String | Yes | Primary Closing Account | Cuenta de cierre principal |
| 68 | `CostAccountingOnly` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Cost Accounting Only | Solo contabilidad de costos |
| 69 | `CostElementRelevant` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Cost Element Relevant | Relevante para elemento de costo |
| 70 | `CostElementCode` | Edm.String | Yes | Cost Element Code | Código de elemento de costo |
| 71 | `StandardAccountCode` | Edm.String | Yes | Standard Account Code | Código de cuenta estándar |
| 72 | `TaxonomyCode` | Edm.String | Yes | Taxonomy Code | Código de taxonomía |
| 73 | `IncomeClassificationCategory` | Edm.Int32 | Yes | Income Classification Category | Categoría de clasificación de ingresos |
| 74 | `IncomeClassificationType` | Edm.Int32 | Yes | Income Classification Type | Tipo de clasificación de ingresos |
| 75 | `ExpenseClassificationCategory` | Edm.Int32 | Yes | Expense Classification Category | Categoría de clasificación de gastos |
| 76 | `ExpenseClassificationType` | Edm.Int32 | Yes | Expense Classification Type | Tipo de clasificación de gastos |
| 77 | `OfficialAccountCode` | Edm.String | Yes | Official Account Code | Código de cuenta oficial |
| 78 | `ExchangeRateDifference` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Exchange Rate Difference | Diferencia de tipo de cambio |

## Navigation properties (54)

Use `GET /b1s/v2/ChartOfAccounts('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `Warehouses` | Collection([Warehouse](../Entidades/Warehouses.md)) | [Warehouses](Warehouses.md) |  | Almacenes |
| `AccrualTypes` | Collection([AccrualType](../Entidades/AccrualTypes.md)) | [AccrualTypes](AccrualTypes.md) |  | Tipos de periodificación |
| `PurchaseQuotations` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseQuotations](PurchaseQuotations.md) |  | Ofertas de compra |
| `ItemGroups` | Collection([ItemGroups](../Entidades/ItemGroups.md)) | [ItemGroups](ItemGroups.md) |  | Grupos de artículos |
| `VatGroups` | Collection([VatGroup](../Entidades/VatGroups.md)) | [VatGroups](VatGroups.md) |  | Grupos de impuestos (IVA) |
| `VendorPayments` | Collection([Payment](../Entidades/VendorPayments.md)) | [VendorPayments](VendorPayments.md) |  | Pagos efectuados |
| `CorrectionInvoiceReversal` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionInvoiceReversal](CorrectionInvoiceReversal.md) |  | Anulación de factura de corrección de clientes |
| `CorrectionInvoice` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionInvoice](CorrectionInvoice.md) |  | Factura de corrección de clientes |
| `WithholdingTaxCodes` | Collection([WithholdingTaxCode](../Entidades/WithholdingTaxCodes.md)) | [WithholdingTaxCodes](WithholdingTaxCodes.md) |  | Códigos de retención de impuestos |
| `PurchaseDeliveryNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseDeliveryNotes](PurchaseDeliveryNotes.md) |  | Pedidos de entrada de mercancías |
| `CorrectionPurchaseInvoice` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionPurchaseInvoice](CorrectionPurchaseInvoice.md) |  | Factura de corrección de proveedores |
| `InventoryGenEntries` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [InventoryGenEntries](InventoryGenEntries.md) |  | Entradas de mercancías |
| `BankPages` | Collection([BankPage](../Entidades/BankPages.md)) | [BankPages](BankPages.md) |  | Páginas de extracto bancario |
| `Items` | Collection([Item](../Entidades/Items.md)) | [Items](Items.md) |  | Artículos |
| `Orders` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Orders](Orders.md) |  | Pedidos de cliente (órdenes de venta) |
| `FAAccountDeterminations` | Collection([FAAccountDetermination](../Entidades/FAAccountDeterminations.md)) | [FAAccountDeterminations](FAAccountDeterminations.md) |  | Determinación de cuentas de activos fijos |
| `WizardPaymentMethods` | Collection([WizardPaymentMethod](../Entidades/WizardPaymentMethods.md)) | [WizardPaymentMethods](WizardPaymentMethods.md) |  | Vías de pago del asistente de pagos |
| `GLAccountAdvancedRules` | Collection([GLAccountAdvancedRule](../Entidades/GLAccountAdvancedRules.md)) | [GLAccountAdvancedRules](GLAccountAdvancedRules.md) |  | Reglas avanzadas de cuentas de mayor |
| `InventoryGenExits` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [InventoryGenExits](InventoryGenExits.md) |  | Salidas de mercancías |
| `Drafts` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Drafts](Drafts.md) |  | Borradores de documentos |
| `AdditionalExpenses` | Collection([AdditionalExpense](../Entidades/AdditionalExpenses.md)) | [AdditionalExpenses](AdditionalExpenses.md) |  | Gastos adicionales (fletes) |
| `CustomsGroups` | Collection([CustomsGroup](../Entidades/CustomsGroups.md)) | [CustomsGroups](CustomsGroups.md) |  | Grupos aduaneros |
| `Currency` | [Currency](../Entidades/Currencies.md) | [Currencies](Currencies.md) | AcctCurrency → Code | Moneda |
| `Project` | [Project](../Entidades/Projects.md) | [Projects](Projects.md) | ProjectCode → Code | Proyecto |
| `AccountCategory` | [AccountCategory](../Entidades/AccountCategory.md) | [AccountCategory](AccountCategory.md) | Category → CategoryCode | Categoría de cuenta |
| `TransactionCode2` | [TransactionCode](../Entidades/TransactionCodes.md) | [TransactionCodes](TransactionCodes.md) | TransactionCode → Code | Códigos de transacción |
| `DistributionRule` | [DistributionRule](../Entidades/DistributionRules.md) | [DistributionRules](DistributionRules.md) | LoadingFactorCode → FactorCode | Norma de reparto |
| `CostElement` | [CostElement](../Entidades/CostElements.md) | [CostElements](CostElements.md) | CostElementCode → Code | Elementos de costo |
| `ReturnRequest` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [ReturnRequest](ReturnRequest.md) |  | Solicitudes de devolución de clientes |
| `DeliveryNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [DeliveryNotes](DeliveryNotes.md) |  | Entregas |
| `PurchaseInvoices` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseInvoices](PurchaseInvoices.md) |  | Facturas de proveedores |
| `SelfInvoices` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [SelfInvoices](SelfInvoices.md) |  | Autofacturas |
| `SalesTaxAuthorities` | Collection([SalesTaxAuthority](../Entidades/SalesTaxAuthorities.md)) | [SalesTaxAuthorities](SalesTaxAuthorities.md) |  | Autoridades del impuesto sobre ventas |
| `Invoices` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Invoices](Invoices.md) |  | Facturas de clientes |
| `CreditNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CreditNotes](CreditNotes.md) |  | Notas de crédito de clientes |
| `PaymentDrafts` | Collection([Payment](../Entidades/VendorPayments.md)) | [PaymentDrafts](PaymentDrafts.md) |  | Borradores de pagos |
| `PurchaseCreditNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseCreditNotes](PurchaseCreditNotes.md) |  | Notas de crédito de proveedores |
| `DunningTerms` | Collection([DunningTerm](../Entidades/DunningTerms.md)) | [DunningTerms](DunningTerms.md) |  | Condiciones de reclamación |
| `BusinessPartners` | Collection([BusinessPartner](../Entidades/BusinessPartners.md)) | [BusinessPartners](BusinessPartners.md) |  | Socios de negocios |
| `DownPayments` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [DownPayments](DownPayments.md) |  | Facturas de anticipo de clientes |
| `PurchaseDownPayments` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseDownPayments](PurchaseDownPayments.md) |  | Facturas de anticipo de proveedores |
| `PurchaseReturns` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseReturns](PurchaseReturns.md) |  | Devoluciones de mercancías a proveedores |
| `PurchaseOrders` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseOrders](PurchaseOrders.md) |  | Pedidos de compra (órdenes de compra) |
| `SelfCreditMemos` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [SelfCreditMemos](SelfCreditMemos.md) |  | Autonotas de crédito |
| `Quotations` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Quotations](Quotations.md) |  | Ofertas de ventas (cotizaciones) |
| `Returns` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Returns](Returns.md) |  | Devoluciones de clientes |
| `HouseBankAccounts` | Collection([HouseBankAccount](../Entidades/HouseBankAccounts.md)) | [HouseBankAccounts](HouseBankAccounts.md) |  | Cuentas bancarias propias |
| `GoodsReturnRequest` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [GoodsReturnRequest](GoodsReturnRequest.md) |  | Solicitudes de devolución de mercancías |
| `CorrectionPurchaseInvoiceReversal` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionPurchaseInvoiceReversal](CorrectionPurchaseInvoiceReversal.md) |  | Anulación de factura de corrección de proveedores |
| `ExpenseTypes` | Collection([ExpenseTypeData](../Entidades/ExpenseTypes.md)) | [ExpenseTypes](ExpenseTypes.md) |  | Tipos de gastos |
| `IncomingPayments` | Collection([Payment](../Entidades/VendorPayments.md)) | [IncomingPayments](IncomingPayments.md) |  | Pagos recibidos |
| `PurchaseRequests` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseRequests](PurchaseRequests.md) |  | Solicitudes de compra |
| `BusinessPlaces` | Collection([BusinessPlace](../Entidades/BusinessPlaces.md)) | [BusinessPlaces](BusinessPlaces.md) |  | Lugares de negocios |
| `CreditCards` | Collection([CreditCard](../Entidades/CreditCards.md)) | [CreditCards](CreditCards.md) |  | Tarjetas de crédito |
