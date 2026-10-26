# BoChangeLogEnum — Objeto del registro de modificaciones

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoChangeLogEnum`
- **Descripción (ES):** Objeto del registro de modificaciones
- **Underlying type:** Edm.Int32
- **Members:** 57

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `clChartOfAccounts` | 0 | Chart Of Accounts | Plan de cuentas |
| `clBusinessPartners` | 1 | Business Partners | Socios de negocios |
| `clItems` | 2 | Items | Artículos |
| `clVatGroups` | 3 | Vat Groups | Grupos de IVA |
| `clUsers` | 4 | Users | Usuarios |
| `clInvoices` | 5 | Invoices | Facturas de clientes |
| `clCreditNotes` | 6 | Credit Notes | Notas de crédito de clientes |
| `clDeliveryNotes` | 7 | Delivery Notes | Entregas |
| `clReturns` | 8 | Returns | Devoluciones |
| `clOrders` | 9 | Orders | Pedidos de cliente |
| `clPurchaseInvoices` | 10 | Purchase Invoices | Facturas de proveedores |
| `clPurchaseCreditNotes` | 11 | Purchase Credit Notes | Notas de crédito de proveedores |
| `clPurchaseDeliveryNotes` | 12 | Purchase Delivery Notes | Pedidos de entrada de mercancías |
| `clPurchaseReturns` | 13 | Purchase Returns | Devoluciones de mercancías |
| `clPurchaseOrders` | 14 | Purchase Orders | Pedidos de compra |
| `clQuotations` | 15 | Quotations | Ofertas de ventas |
| `clIncomingPayments` | 16 | Incoming Payments | Pagos recibidos |
| `clJournalEntries` | 17 | Journal Entries | Asientos contables |
| `clCreditCards` | 18 | Credit Cards | Tarjetas de crédito |
| `clAdminInfo` | 19 | Admin Information | Datos de administración |
| `clVendorPayments` | 20 | Vendor Payments | Pagos efectuados |
| `clItemGroups` | 21 | Item Groups | Grupos de artículos |
| `clInventoryGeneralEntry` | 22 | Inventory General Entry | Entradas de mercancías |
| `clInventoryGeneralExit` | 23 | Inventory General Exit | Salidas de mercancías |
| `clWarehouses` | 24 | Warehouses | Almacenes |
| `clProductTrees` | 25 | Product Trees | Listas de materiales |
| `clStockTransfers` | 26 | Stock Transfers | Transferencias de stock |
| `clFinancePeriods` | 27 | Finance Periods | Períodos contables |
| `clAdditionalExpenses` | 28 | Additional Expenses | Gastos adicionales |
| `clPickLists` | 29 | Pick Lists | Listas de picking |
| `clMaterialRevaluation` | 30 | Material Revaluation | Revalorización de inventario |
| `clCorrectionPurchaseInvoice` | 31 | Correction Purchase Invoice | Factura de corrección de proveedores |
| `clCorrectionPurchaseInvoiceReversal` | 32 | Correction Purchase Invoice Reversal | Anulación de factura de corrección de proveedores |
| `clCorrectionInvoice` | 33 | Correction Invoice | Factura de corrección de clientes |
| `clCorrectionInvoiceReversal` | 34 | Correction Invoice Reversal | Anulación de factura de corrección de clientes |
| `clEmployeesInfo` | 35 | Employees Information | Empleados |
| `clCustomerEquipmentCards` | 36 | Customer Equipment Cards | Tarjetas de equipo del cliente |
| `clWithholdingTaxCodes` | 37 | Withholding Tax Codes | Códigos de retención |
| `clBillOfExchange` | 38 | Bill Of Exchange | Letras de cambio |
| `clServiceCalls` | 39 | Service Calls | Llamadas de servicio |
| `clProductionOrders` | 40 | Production Orders | Órdenes de fabricación |
| `clDownPayments` | 41 | Down Payments | Anticipos de clientes |
| `clPurchaseDownPayments` | 42 | Purchase Down Payments | Anticipos de proveedores |
| `clPeriodCategory` | 43 | Period Category | Categoría de períodos |
| `clHouseBankAccounts` | 44 | House Bank Accounts | Cuentas bancarias propias |
| `clSalesTaxInvoice` | 45 | Sales Tax Invoice | Factura de impuestos de venta |
| `clPurchaseTaxInvoice` | 46 | Purchase Tax Invoice | Factura de impuestos de compra |
| `clExternalBankOperationCodes` | 47 | External Bank Operation Codes | Códigos de operación bancaria externa |
| `clInternalBankOperationCodes` | 48 | Internal Bank Operation Codes | Códigos de operación bancaria interna |
| `clOutgoingExciseInvoice` | 49 | Outgoing Excise Invoice | Factura de impuestos especiales saliente |
| `clIncomingExciseInvoice` | 50 | Incoming Excise Invoice | Factura de impuestos especiales entrante |
| `clInventoryTransferRequests` | 51 | Inventory Transfer Requests | Solicitudes de transferencia de stock |
| `clPurchaseQuotation` | 52 | Purchase Quotation | Oferta de compra |
| `clActivities` | 53 | Activities | Actividades |
| `clChecksForPayment` | 54 | Checks For Payment | Cheques para pago |
| `clServiceContract` | 55 | Service Contract | Contrato de servicio |
| `clUDO` | 100 | UDO | Objeto definido por el usuario (UDO) |

## Used by (2 properties)

- [GetChangeLogParams](../Tipos-Complejos/GetChangeLogParams.md).`Object`
- [ShowDifferenceParams](../Tipos-Complejos/ShowDifferenceParams.md).`Object`
