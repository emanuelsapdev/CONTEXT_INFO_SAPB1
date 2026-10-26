# PaymentTermsTypes — Condiciones de pago

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `PaymentTermsTypes`
- **Descripción (ES):** Condiciones de pago
- **Entity type:** `PaymentTermsType` (open type: accepts dynamic/UDF properties)
- **Key:** `GroupNumber` (Edm.Int32)
- **DB tables (main / lines):** [OCTG](../../Tablas%20SAP%20B1/OCTG.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 17 · **Navigation properties:** 33 · **Bound actions:** 1

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/PaymentTermsTypes?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/PaymentTermsTypes/$count` | Contar |
| Get by key | `GET /b1s/v2/PaymentTermsTypes(1)` | Obtener por clave |
| Create | `POST /b1s/v2/PaymentTermsTypes` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/PaymentTermsTypes(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/PaymentTermsTypes(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/PaymentTermsTypes(1)` (only if the B1 object allows removal) | Borrar |
| Action `Close` | `POST /b1s/v2/PaymentTermsTypes(1)/Close` | Cerrar |

## Properties (17)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `GroupNumber` 🔑 | Edm.Int32 | No | Group Number | Número de grupo |
| 2 | `PaymentTermsGroupName` | Edm.String | Yes | Payment Terms Group Name | Nombre de las condiciones de pago |
| 3 | `StartFrom` | [BoPayTermDueTypes](../Enums/BoPayTermDueTypes.md) | Yes | Start From | Comenzar desde |
| 4 | `NumberOfAdditionalMonths` | Edm.Int32 | Yes | Number Of Additional Months | Cantidad de meses adicionales |
| 5 | `NumberOfAdditionalDays` | Edm.Int32 | Yes | Number Of Additional Days | Cantidad de días adicionales |
| 6 | `CreditLimit` | Edm.Double | Yes | Credit Limit | Límite de crédito |
| 7 | `GeneralDiscount` | Edm.Double | Yes | General Discount | Descuento general |
| 8 | `InterestOnArrears` | Edm.Double | Yes | Interest On Arrears | Intereses por mora |
| 9 | `PriceListNo` | Edm.Int32 | Yes | Price List Number | Número de lista de precios |
| 10 | `LoadLimit` | Edm.Double | Yes | Load Limit | Límite de carga |
| 11 | `OpenReceipt` | [BoOpenIncPayment](../Enums/BoOpenIncPayment.md) | Yes | Open Receipt | Recibo abierto |
| 12 | `DiscountCode` | Edm.String | Yes | Discount Code | Código de descuento |
| 13 | `DunningCode` | Edm.String | Yes | Dunning Code | Código de reclamación |
| 14 | `BaselineDate` | [BoBaselineDate](../Enums/BoBaselineDate.md) | Yes | Baseline Date | Fecha de referencia |
| 15 | `NumberOfInstallments` | Edm.Int32 | Yes | Number Of Installments | Cantidad de cuotas |
| 16 | `NumberOfToleranceDays` | Edm.Int32 | Yes | Number Of Tolerance Days | Cantidad de días de tolerancia |
| 17 | `EndAt` | [BoPayTermDueTypes](../Enums/BoPayTermDueTypes.md) | Yes | End At | Finaliza en |

## Navigation properties (33)

Use `GET /b1s/v2/PaymentTermsTypes(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `PurchaseQuotations` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseQuotations](PurchaseQuotations.md) |  | Ofertas de compra |
| `CorrectionInvoiceReversal` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionInvoiceReversal](CorrectionInvoiceReversal.md) |  | Anulación de factura de corrección de clientes |
| `CorrectionInvoice` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionInvoice](CorrectionInvoice.md) |  | Factura de corrección de clientes |
| `PurchaseDeliveryNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseDeliveryNotes](PurchaseDeliveryNotes.md) |  | Pedidos de entrada de mercancías |
| `CorrectionPurchaseInvoice` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionPurchaseInvoice](CorrectionPurchaseInvoice.md) |  | Factura de corrección de proveedores |
| `InventoryGenEntries` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [InventoryGenEntries](InventoryGenEntries.md) |  | Entradas de mercancías |
| `Orders` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Orders](Orders.md) |  | Pedidos de cliente (órdenes de venta) |
| `WizardPaymentMethods` | Collection([WizardPaymentMethod](../Entidades/WizardPaymentMethods.md)) | [WizardPaymentMethods](WizardPaymentMethods.md) |  | Vías de pago del asistente de pagos |
| `InventoryGenExits` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [InventoryGenExits](InventoryGenExits.md) |  | Salidas de mercancías |
| `Drafts` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Drafts](Drafts.md) |  | Borradores de documentos |
| `InventoryTransferRequests` | Collection([StockTransfer](../Entidades/StockTransfers.md)) | [InventoryTransferRequests](InventoryTransferRequests.md) |  | Solicitudes de transferencia de stock |
| `ReturnRequest` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [ReturnRequest](ReturnRequest.md) |  | Solicitudes de devolución de clientes |
| `DeliveryNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [DeliveryNotes](DeliveryNotes.md) |  | Entregas |
| `PurchaseInvoices` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseInvoices](PurchaseInvoices.md) |  | Facturas de proveedores |
| `StockTransferDrafts` | Collection([StockTransfer](../Entidades/StockTransfers.md)) | [StockTransferDrafts](StockTransferDrafts.md) |  | Borradores de transferencias de stock |
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
| `PriceList` | [PriceList](../Entidades/PriceLists.md) | [PriceLists](PriceLists.md) | PriceListNo → PriceListNo | Lista de precios |
| `CashDiscount` | [CashDiscount](../Entidades/CashDiscounts.md) | [CashDiscounts](CashDiscounts.md) | DiscountCode → Code | Descuento por pronto pago |
| `CorrectionPurchaseInvoiceReversal` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionPurchaseInvoiceReversal](CorrectionPurchaseInvoiceReversal.md) |  | Anulación de factura de corrección de proveedores |
| `PurchaseRequests` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseRequests](PurchaseRequests.md) |  | Solicitudes de compra |

## Bound actions (1)

### Close

- **Descripción (ES):** Cerrar
- **Request:** `POST /b1s/v2/PaymentTermsTypes(1)/Close`


## Service operations that use this type

- [`PaymentTermsTypesService_UpdateWithBPs`](../Servicios/PaymentTermsTypesService.md#paymenttermstypesservice_updatewithbps)
