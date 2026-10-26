# WizardPaymentMethods — Vías de pago del asistente de pagos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `WizardPaymentMethods`
- **Descripción (ES):** Vías de pago del asistente de pagos
- **Entity type:** `WizardPaymentMethod` (open type: accepts dynamic/UDF properties)
- **Key:** `PaymentMethodCode` (Edm.String)
- **DB tables (main / lines):** [OPYM](../../Tablas%20SAP%20B1/OPYM.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 52 · **Navigation properties:** 33 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/WizardPaymentMethods?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/WizardPaymentMethods/$count` | Contar |
| Get by key | `GET /b1s/v2/WizardPaymentMethods('value')` | Obtener por clave |
| Create | `POST /b1s/v2/WizardPaymentMethods` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/WizardPaymentMethods('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/WizardPaymentMethods('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/WizardPaymentMethods('value')` (only if the B1 object allows removal) | Borrar |

## Properties (52)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `PaymentMethodCode` 🔑 | Edm.String | No | Payment Method Code | Código de vía de pago |
| 2 | `Description` | Edm.String | Yes | Description | Descripción |
| 3 | `Type` | [BoPaymentTypeEnum](../Enums/BoPaymentTypeEnum.md) | Yes | Type | Tipo |
| 4 | `PaymentMeans` | [BoPaymentMeansEnum](../Enums/BoPaymentMeansEnum.md) | Yes | Payment Means | Medio de pago |
| 5 | `CheckAddress` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Check Address | Dirección del cheque |
| 6 | `CheckBankDetails` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Check Bank Details | Verificar datos bancarios |
| 7 | `CollectionAuthorizationCheck` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Collection Authorization Check | Verificación de autorización de cobro |
| 8 | `BlockForeignPayment` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Block Foreign Payment | Bloquear pago al exterior |
| 9 | `BlockForeignBank` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Block Foreign Bank | Bloquear banco extranjero |
| 10 | `CurrencyRestriction` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Currency Restriction | Restricción de moneda |
| 11 | `PostOfficeBank` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Post Office Bank | Banco postal |
| 12 | `MinimumAmount` | Edm.Double | Yes | Minimum Amount | Importe mínimo |
| 13 | `MaximumAmount` | Edm.Double | Yes | Maximum Amount | Importe máximo |
| 14 | `DefaultBank` | Edm.String | Yes | Default Bank | Banco predeterminado |
| 15 | `UserSignature` | Edm.Int32 | Yes | User Signature | Firma del usuario |
| 16 | `CreationDate` | Edm.DateTimeOffset | Yes | Creation Date | Fecha de creación |
| 17 | `BankCountry` | Edm.String | Yes | Bank Country | País del banco |
| 18 | `DefaultAccount` | Edm.String | Yes | Default Account | Cuenta predeterminada |
| 19 | `GLAccount` | Edm.String | Yes | G/L Account | Cuenta de mayor |
| 20 | `Branch` | Edm.String | Yes | Branch | Sucursal |
| 21 | `KeyCode` | Edm.String | Yes | Key Code | Código de clave |
| 22 | `TransactionType` | Edm.String | Yes | Transaction Type | Tipo de transacción |
| 23 | `Format` | Edm.String | Yes | Format | Formato |
| 24 | `AgentCollection` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Agent Collection | Colección de agentes |
| 25 | `SendforAcceptance` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Sendfor Acceptance | Enviar para aceptación |
| 26 | `GroupByDate` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Group By Date | Agrupar por fecha |
| 27 | `DepositNorm` | Edm.String | Yes | Deposit Norm | Norma del depósito |
| 28 | `DebitMemo` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Debit Memo | Nota de débito |
| 29 | `GroupByPaymentReference` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Group By Payment Reference | Agrupar por referencia de pago |
| 30 | `GroupInvoicesbyPay` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Group Invoicesby Pay | Agrupar facturas por pago |
| 31 | `DueDateSelection` | [BoDueDateEnum](../Enums/BoDueDateEnum.md) | Yes | Due Date Selection | Selección de fecha de vencimiento |
| 32 | `PaymentTermsCode` | Edm.Int32 | Yes | Payment Terms Code | Código de condiciones de pago |
| 33 | `PosttoGLInterimAccount` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Postto G/L Interim Account | Contabilizar en cuenta transitoria de mayor |
| 34 | `BankAccountKey` | Edm.Int32 | Yes | Bank Account Key | Clave de la cuenta bancaria |
| 35 | `DocType` | Edm.String | Yes | Document Type | Tipo de documento (artículos/servicios) |
| 36 | `Accepted` | Edm.String | Yes | Accepted | Aceptado |
| 37 | `PortfolioID` | Edm.String | Yes | Portfolio ID | ID de cartera |
| 38 | `CurCode` | Edm.String | Yes | Currency Code | Código de moneda |
| 39 | `Instruction1` | Edm.String | Yes | Instruction 1 | Instrucción 1 |
| 40 | `Instruction2` | Edm.String | Yes | Instruction 2 | Instrucción 2 |
| 41 | `PaymentPlace` | Edm.String | Yes | Payment Place | Lugar de pago |
| 42 | `BarcodeDll` | Edm.String | Yes | Barcode Dll | DLL de código de barras |
| 43 | `Active` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Active | Activo |
| 44 | `GroupInvoicesByPayToBank` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Group Invoices By Pay To Bank | Agrupar facturas por banco de pago |
| 45 | `GroupInvoicesByCurrency` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Group Invoices By Currency | Agrupar facturas por moneda |
| 46 | `BankChargeRate` | Edm.Double | Yes | Bank Charge Rate | Tasa de comisión bancaria |
| 47 | `ReportCode` | Edm.String | Yes | Report Code | Código de informe |
| 48 | `CancelInstruction` | Edm.String | Yes | Cancel Instruction | Instrucción de cancelación |
| 49 | `OccurenceCode` | Edm.String | Yes | Occurence Code | Código de ocurrencia |
| 50 | `MovementCode` | Edm.String | Yes | Movement Code | Código de movimiento |
| 51 | `DirectDebit` | Edm.String | Yes | Direct Debit | Débito directo |
| 52 | `CurrencyRestrictions` | Collection([CurrencyRestriction](../Tipos-Complejos/CurrencyRestriction.md)) | Yes | Currency Restrictions | Restricciones de moneda |

## Navigation properties (33)

Use `GET /b1s/v2/WizardPaymentMethods('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `PurchaseQuotations` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseQuotations](PurchaseQuotations.md) |  | Ofertas de compra |
| `CorrectionInvoiceReversal` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionInvoiceReversal](CorrectionInvoiceReversal.md) |  | Anulación de factura de corrección de clientes |
| `CorrectionInvoice` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionInvoice](CorrectionInvoice.md) |  | Factura de corrección de clientes |
| `PurchaseDeliveryNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseDeliveryNotes](PurchaseDeliveryNotes.md) |  | Pedidos de entrada de mercancías |
| `CorrectionPurchaseInvoice` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionPurchaseInvoice](CorrectionPurchaseInvoice.md) |  | Factura de corrección de proveedores |
| `InventoryGenEntries` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [InventoryGenEntries](InventoryGenEntries.md) |  | Entradas de mercancías |
| `Orders` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Orders](Orders.md) |  | Pedidos de cliente (órdenes de venta) |
| `User` | [User](../Entidades/Users.md) | [Users](Users.md) | UserSignature → InternalKey | Usuario |
| `Country` | [Country](../Entidades/Countries.md) | [Countries](Countries.md) | BankCountry → Code | País |
| `ChartOfAccount` | [ChartOfAccount](../Entidades/ChartOfAccounts.md) | [ChartOfAccounts](ChartOfAccounts.md) | GLAccount → Code | Plan de cuentas (cuentas de mayor) |
| `PaymentTermsType` | [PaymentTermsType](../Entidades/PaymentTermsTypes.md) | [PaymentTermsTypes](PaymentTermsTypes.md) | PaymentTermsCode → GroupNumber | Condiciones de pago |
| `HouseBankAccount` | [HouseBankAccount](../Entidades/HouseBankAccounts.md) | [HouseBankAccounts](HouseBankAccounts.md) | BankAccountKey → AbsoluteEntry | Cuenta bancaria propia |
| `InventoryGenExits` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [InventoryGenExits](InventoryGenExits.md) |  | Salidas de mercancías |
| `Drafts` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Drafts](Drafts.md) |  | Borradores de documentos |
| `ReturnRequest` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [ReturnRequest](ReturnRequest.md) |  | Solicitudes de devolución de clientes |
| `DeliveryNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [DeliveryNotes](DeliveryNotes.md) |  | Entregas |
| `PurchaseInvoices` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseInvoices](PurchaseInvoices.md) |  | Facturas de proveedores |
| `SelfInvoices` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [SelfInvoices](SelfInvoices.md) |  | Autofacturas |
| `BlanketAgreements` | Collection([BlanketAgreement](../Entidades/BlanketAgreements.md)) | [BlanketAgreements](BlanketAgreements.md) |  | Acuerdos globales |
| `Invoices` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Invoices](Invoices.md) |  | Facturas de clientes |
| `CreditNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CreditNotes](CreditNotes.md) |  | Notas de crédito de clientes |
| `PurchaseCreditNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseCreditNotes](PurchaseCreditNotes.md) |  | Notas de crédito de proveedores |
| `BusinessPartners` | Collection([BusinessPartner](../Entidades/BusinessPartners.md)) | [BusinessPartners](BusinessPartners.md) |  | Socios de negocios |
| `DownPayments` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [DownPayments](DownPayments.md) |  | Facturas de anticipo de clientes |
| `PurchaseDownPayments` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseDownPayments](PurchaseDownPayments.md) |  | Facturas de anticipo de proveedores |
| `PurchaseReturns` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseReturns](PurchaseReturns.md) |  | Devoluciones de mercancías a proveedores |
| `PurchaseOrders` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseOrders](PurchaseOrders.md) |  | Pedidos de compra (órdenes de compra) |
| `SelfCreditMemos` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [SelfCreditMemos](SelfCreditMemos.md) |  | Autonotas de crédito |
| `Quotations` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Quotations](Quotations.md) |  | Ofertas de ventas (cotizaciones) |
| `Returns` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Returns](Returns.md) |  | Devoluciones de clientes |
| `GoodsReturnRequest` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [GoodsReturnRequest](GoodsReturnRequest.md) |  | Solicitudes de devolución de mercancías |
| `CorrectionPurchaseInvoiceReversal` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionPurchaseInvoiceReversal](CorrectionPurchaseInvoiceReversal.md) |  | Anulación de factura de corrección de proveedores |
| `PurchaseRequests` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseRequests](PurchaseRequests.md) |  | Solicitudes de compra |
