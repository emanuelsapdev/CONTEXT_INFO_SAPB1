# ReferencedObjectTypeEnum — Tipo de objeto referenciado

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `ReferencedObjectTypeEnum`
- **Descripción (ES):** Tipo de objeto referenciado
- **Underlying type:** Edm.Int32
- **Members:** 38

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `rot_ExternalDocument` | -1 | External Document | Documento externo |
| `rot_SalesQuotation` | 23 | Sales Quotation | Oferta de ventas |
| `rot_SalesOrder` | 17 | Sales Order | Pedido de cliente |
| `rot_DeliveryNotes` | 15 | Delivery Notes | Entrega |
| `rot_ReturnRequest` | 234000031 | Return Request | Solicitud de devolución |
| `rot_Return` | 16 | Return | Devolución |
| `rot_DownPaymentIncoming` | 203 | Down Payment Incoming | Anticipo de clientes |
| `rot_SalesInvoice` | 13 | Sales Invoice | Factura de clientes |
| `rot_SalesCreditNote` | 14 | Sales Credit Note | Nota de crédito de clientes |
| `rot_CorrectionSalesInvoice` | 165 | Correction Sales Invoice | Factura de corrección de clientes |
| `rot_SalesTaxInvoice` | 280 | Sales Tax Invoice | Factura de impuestos de venta |
| `rot_PurchaseQuotation` | 540000006 | Purchase Quotation | Oferta de compra |
| `rot_PurchaseOrder` | 22 | Purchase Order | Pedido de compra |
| `rot_GoodsReceiptPO` | 20 | Goods Receipt PO | Pedido de entrada de mercancías |
| `rot_GoodsReturnRequest` | 234000032 | Goods Return Request | Solicitud de devolución de mercancías |
| `rot_GoodsReturn` | 21 | Goods Return | Devolución de mercancías |
| `rot_DownPaymentOutgoing` | 204 | Down Payment Outgoing | Anticipo de proveedores |
| `rot_PurchaseInvoice` | 18 | Purchase Invoice | Factura de proveedores |
| `rot_PurchaseCreditNote` | 19 | Purchase Credit Note | Nota de crédito de proveedores |
| `rot_CorrectionPurchaseInvoice` | 163 | Correction Purchase Invoice | Factura de corrección de proveedores |
| `rot_PurchaseTaxInvoice` | 281 | Purchase Tax Invoice | Factura de impuestos de compra |
| `rot_LandedCosts` | 69 | Landed Costs | Costos de importación |
| `rot_IncomingPayments` | 24 | Incoming Payments | Pagos recibidos |
| `rot_JournalEntry` | 30 | Journal Entry | Asiento contable |
| `rot_ProductionOrder` | 202 | Production Order | Orden de fabricación |
| `rot_InternalReconciliation` | 321 | Internal Reconciliation | Conciliación interna |
| `rot_OriginalInvoice` | 13001 | Original Invoice | Factura original |
| `rot_OriginalARDownPayment` | 20301 | Original AR Down Payment | Anticipo de clientes original |
| `rot_PurchaseRequest` | 1470000113 | Purchase Request | Solicitud de compra |
| `rot_GoodsReceipt` | 59 | Goods Receipt | Entrada de mercancías |
| `rot_GoodsIssue` | 60 | Goods Issue | Salida de mercancías |
| `rot_InventoryTransferRequest` | 1250000001 | Inventory Transfer Request | Solicitud de transferencia de stock |
| `rot_InventoryTransfer` | 67 | Inventory Transfer | Transferencia de stock |
| `rot_ChecksforPayment` | 57 | Checksfor Payment | Cheques para pago |
| `rot_MaterialRevaluation` | 162 | Material Revaluation | Revalorización de inventario |
| `rot_InventoryCounting` | 1470000065 | Inventory Counting | Recuento de inventario |
| `rot_InventoryPosting` | 10000071 | Inventory Posting | Contabilización de inventario |
| `rot_OutgoingPayments` | 46 | Outgoing Payments | Pagos efectuados |

## Used by (10 properties)

- [ChecksforPaymentDocumentReference](../Tipos-Complejos/ChecksforPaymentDocumentReference.md).`ReferencedObjectType`
- [DocumentReference](../Tipos-Complejos/DocumentReference.md).`RefObjType`
- [InventoryCountingDocumentReferences](../Tipos-Complejos/InventoryCountingDocumentReferences.md).`ReferencedObjectType`
- [InventoryPostingDocumentReferences](../Tipos-Complejos/InventoryPostingDocumentReferences.md).`ReferencedObjectType`
- [MaterialRevaluationDocumentReferences](../Tipos-Complejos/MaterialRevaluationDocumentReferences.md).`ReferencedObjectType`
- [PaymentDocumentReferences](../Tipos-Complejos/PaymentDocumentReferences.md).`ReferencedObjectType`
- [ProductionOrdersDocumentReference](../Tipos-Complejos/ProductionOrdersDocumentReference.md).`RefObjType`
- [PurchaseTaxInvoiceDocumentReference](../Tipos-Complejos/PurchaseTaxInvoiceDocumentReference.md).`ReferencedObjectType`
- [RecurringPostingsDocumentReference](../Tipos-Complejos/RecurringPostingsDocumentReference.md).`ReferencedObjectType`
- [SalesTaxInvoiceDocumentReference](../Tipos-Complejos/SalesTaxInvoiceDocumentReference.md).`ReferencedObjectType`
