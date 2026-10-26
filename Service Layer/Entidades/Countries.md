# Countries — Países/Regiones

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `Countries`
- **Descripción (ES):** Países/Regiones
- **Entity type:** `Country` (open type: accepts dynamic/UDF properties)
- **Key:** `Code` (Edm.String)
- **DB tables (main / lines):** [OCRY](../../Tablas%20SAP%20B1/OCRY.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 18 · **Navigation properties:** 47 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/Countries?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/Countries/$count` | Contar |
| Get by key | `GET /b1s/v2/Countries('value')` | Obtener por clave |
| Create | `POST /b1s/v2/Countries` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/Countries('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/Countries('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/Countries('value')` (only if the B1 object allows removal) | Borrar |

## Properties (18)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.String | No | Code | Código |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `CodeForReports` | Edm.String | Yes | Code For Reports | Código para informes |
| 4 | `AddressFormat` | Edm.Int32 | Yes | Address Format | Formato de dirección |
| 5 | `EU` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | EU | Unión Europea |
| 6 | `NumberOfDigitsForTaxID` | Edm.Int32 | Yes | Number Of Digits For Tax ID | Cantidad de dígitos del ID fiscal |
| 7 | `BankCodeDigits` | Edm.Int32 | Yes | Bank Code Digits | Dígitos del código bancario |
| 8 | `BankBranchDigits` | Edm.Int32 | Yes | Bank Branch Digits | Dígitos de la sucursal bancaria |
| 9 | `BankAccountDigits` | Edm.Int32 | Yes | Bank Account Digits | Dígitos de la cuenta bancaria |
| 10 | `BankControlKeyDigits` | Edm.Int32 | Yes | Bank Control Key Digits | Dígitos de clave de control bancaria |
| 11 | `DomesticAccountValidation` | [DomesticBankAccountValidationEnum](../Enums/DomesticBankAccountValidationEnum.md) | Yes | Domestic Account Validation | Validación de cuenta nacional |
| 12 | `IbanValidation` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Iban Validation | Validación de IBAN |
| 13 | `Blacklisted` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Blacklisted | En lista negra |
| 14 | `UICCountryCode` | Edm.String | Yes | UIC Country Code | Código de país UIC |
| 15 | `EAEU` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | EAEU | Unión Económica Euroasiática |
| 16 | `ISOAlpha2Code` | Edm.String | Yes | ISO Alpha 2 Code | Código ISO alfa-2 |
| 17 | `ISOAlpha3Code` | Edm.String | Yes | ISO Alpha 3 Code | Código ISO alfa-3 |
| 18 | `ISONumeric` | Edm.String | Yes | ISO Numeric | Código ISO numérico |

## Navigation properties (47)

Use `GET /b1s/v2/Countries('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `UserDefaultGroups` | Collection([UserDefaultGroup](../Entidades/UserDefaultGroups.md)) | [UserDefaultGroups](UserDefaultGroups.md) |  | Grupos de valores predeterminados de usuario |
| `Warehouses` | Collection([Warehouse](../Entidades/Warehouses.md)) | [Warehouses](Warehouses.md) |  | Almacenes |
| `ChecksforPayment` | Collection([ChecksforPayment](../Entidades/ChecksforPayment.md)) | [ChecksforPayment](ChecksforPayment.md) |  | Cheques para pago |
| `PurchaseQuotations` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseQuotations](PurchaseQuotations.md) |  | Ofertas de compra |
| `VendorPayments` | Collection([Payment](../Entidades/VendorPayments.md)) | [VendorPayments](VendorPayments.md) |  | Pagos efectuados |
| `CorrectionInvoiceReversal` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionInvoiceReversal](CorrectionInvoiceReversal.md) |  | Anulación de factura de corrección de clientes |
| `CustomerEquipmentCards` | Collection([CustomerEquipmentCard](../Entidades/CustomerEquipmentCards.md)) | [CustomerEquipmentCards](CustomerEquipmentCards.md) |  | Tarjetas de equipo del cliente |
| `CorrectionInvoice` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionInvoice](CorrectionInvoice.md) |  | Factura de corrección de clientes |
| `PurchaseDeliveryNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseDeliveryNotes](PurchaseDeliveryNotes.md) |  | Pedidos de entrada de mercancías |
| `CorrectionPurchaseInvoice` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionPurchaseInvoice](CorrectionPurchaseInvoice.md) |  | Factura de corrección de proveedores |
| `InventoryGenEntries` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [InventoryGenEntries](InventoryGenEntries.md) |  | Entradas de mercancías |
| `WarehouseLocations` | Collection([WarehouseLocation](../Entidades/WarehouseLocations.md)) | [WarehouseLocations](WarehouseLocations.md) |  | Ubicaciones de almacenes |
| `ServiceCalls` | Collection([ServiceCall](../Entidades/ServiceCalls.md)) | [ServiceCalls](ServiceCalls.md) |  | Llamadas de servicio |
| `EmployeesInfo` | Collection([EmployeeInfo](../Entidades/EmployeesInfo.md)) | [EmployeesInfo](EmployeesInfo.md) |  | Empleados |
| `Orders` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Orders](Orders.md) |  | Pedidos de cliente (órdenes de venta) |
| `WizardPaymentMethods` | Collection([WizardPaymentMethod](../Entidades/WizardPaymentMethods.md)) | [WizardPaymentMethods](WizardPaymentMethods.md) |  | Vías de pago del asistente de pagos |
| `GLAccountAdvancedRules` | Collection([GLAccountAdvancedRule](../Entidades/GLAccountAdvancedRules.md)) | [GLAccountAdvancedRules](GLAccountAdvancedRules.md) |  | Reglas avanzadas de cuentas de mayor |
| `InventoryGenExits` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [InventoryGenExits](InventoryGenExits.md) |  | Salidas de mercancías |
| `Drafts` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Drafts](Drafts.md) |  | Borradores de documentos |
| `ExportDeterminations` | Collection([ExportDetermination](../Entidades/ExportDeterminations.md)) | [ExportDeterminations](ExportDeterminations.md) |  | Determinaciones de exportación |
| `ReturnRequest` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [ReturnRequest](ReturnRequest.md) |  | Solicitudes de devolución de clientes |
| `DeliveryNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [DeliveryNotes](DeliveryNotes.md) |  | Entregas |
| `PurchaseInvoices` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseInvoices](PurchaseInvoices.md) |  | Facturas de proveedores |
| `SelfInvoices` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [SelfInvoices](SelfInvoices.md) |  | Autofacturas |
| `Invoices` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Invoices](Invoices.md) |  | Facturas de clientes |
| `States` | Collection([State](../Entidades/States.md)) | [States](States.md) |  | Estados/Provincias |
| `CreditNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CreditNotes](CreditNotes.md) |  | Notas de crédito de clientes |
| `PaymentDrafts` | Collection([Payment](../Entidades/VendorPayments.md)) | [PaymentDrafts](PaymentDrafts.md) |  | Borradores de pagos |
| `Banks` | Collection([Bank](../Entidades/Banks.md)) | [Banks](Banks.md) |  | Bancos |
| `Contacts` | Collection([Contact](../Entidades/Contacts.md)) | [Contacts](Contacts.md) |  | Contactos |
| `PurchaseCreditNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseCreditNotes](PurchaseCreditNotes.md) |  | Notas de crédito de proveedores |
| `BusinessPartners` | Collection([BusinessPartner](../Entidades/BusinessPartners.md)) | [BusinessPartners](BusinessPartners.md) |  | Socios de negocios |
| `DownPayments` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [DownPayments](DownPayments.md) |  | Facturas de anticipo de clientes |
| `PurchaseDownPayments` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseDownPayments](PurchaseDownPayments.md) |  | Facturas de anticipo de proveedores |
| `PurchaseReturns` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseReturns](PurchaseReturns.md) |  | Devoluciones de mercancías a proveedores |
| `Activities` | Collection([Activity](../Entidades/Activities.md)) | [Activities](Activities.md) |  | Actividades |
| `PurchaseOrders` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseOrders](PurchaseOrders.md) |  | Pedidos de compra (órdenes de compra) |
| `SelfCreditMemos` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [SelfCreditMemos](SelfCreditMemos.md) |  | Autonotas de crédito |
| `Quotations` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Quotations](Quotations.md) |  | Ofertas de ventas (cotizaciones) |
| `Returns` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Returns](Returns.md) |  | Devoluciones de clientes |
| `HouseBankAccounts` | Collection([HouseBankAccount](../Entidades/HouseBankAccounts.md)) | [HouseBankAccounts](HouseBankAccounts.md) |  | Cuentas bancarias propias |
| `GoodsReturnRequest` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [GoodsReturnRequest](GoodsReturnRequest.md) |  | Solicitudes de devolución de mercancías |
| `CorrectionPurchaseInvoiceReversal` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionPurchaseInvoiceReversal](CorrectionPurchaseInvoiceReversal.md) |  | Anulación de factura de corrección de proveedores |
| `IncomingPayments` | Collection([Payment](../Entidades/VendorPayments.md)) | [IncomingPayments](IncomingPayments.md) |  | Pagos recibidos |
| `PurchaseRequests` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseRequests](PurchaseRequests.md) |  | Solicitudes de compra |
| `BusinessPlaces` | Collection([BusinessPlace](../Entidades/BusinessPlaces.md)) | [BusinessPlaces](BusinessPlaces.md) |  | Lugares de negocios |
| `CreditCards` | Collection([CreditCard](../Entidades/CreditCards.md)) | [CreditCards](CreditCards.md) |  | Tarjetas de crédito |
