# DocumentCloseParams — Parámetros de cierre de documento

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `DocumentCloseParams`
- **Descripción (ES):** Parámetros de cierre de documento
- **Description (EN):** Document Close Parameters

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 2 | `ClosingOption` | [ClosingOptionEnum](../Enums/ClosingOptionEnum.md) | Yes | Closing Option | Opción de cierre |
| 3 | `SpecifiedClosingDate` | Edm.DateTimeOffset | Yes | Specified Closing Date | Fecha de cierre especificada |

## Used by (service operations)

- [`CorrectionInvoiceReversalService_CloseByDate`](../Servicios/CorrectionInvoiceReversalService.md#correctioninvoicereversalservice_closebydate)
- [`CorrectionInvoiceService_CloseByDate`](../Servicios/CorrectionInvoiceService.md#correctioninvoiceservice_closebydate)
- [`CorrectionPurchaseInvoiceReversalService_CloseByDate`](../Servicios/CorrectionPurchaseInvoiceReversalService.md#correctionpurchaseinvoicereversalservice_closebydate)
- [`CorrectionPurchaseInvoiceService_CloseByDate`](../Servicios/CorrectionPurchaseInvoiceService.md#correctionpurchaseinvoiceservice_closebydate)
- [`CreditNotesService_CloseByDate`](../Servicios/CreditNotesService.md#creditnotesservice_closebydate)
- [`DeliveryNotesService_CloseByDate`](../Servicios/DeliveryNotesService.md#deliverynotesservice_closebydate)
- [`DownPaymentsService_CloseByDate`](../Servicios/DownPaymentsService.md#downpaymentsservice_closebydate)
- [`DraftsService_CloseByDate`](../Servicios/DraftsService.md#draftsservice_closebydate)
- [`GoodsReturnRequestService_CloseByDate`](../Servicios/GoodsReturnRequestService.md#goodsreturnrequestservice_closebydate)
- [`InventoryGenEntryService_CloseByDate`](../Servicios/InventoryGenEntryService.md#inventorygenentryservice_closebydate)
- [`InventoryGenExitService_CloseByDate`](../Servicios/InventoryGenExitService.md#inventorygenexitservice_closebydate)
- [`InvoicesService_CloseByDate`](../Servicios/InvoicesService.md#invoicesservice_closebydate)
- [`OrdersService_CloseByDate`](../Servicios/OrdersService.md#ordersservice_closebydate)
- [`PurchaseCreditNotesService_CloseByDate`](../Servicios/PurchaseCreditNotesService.md#purchasecreditnotesservice_closebydate)
- [`PurchaseDeliveryNotesService_CloseByDate`](../Servicios/PurchaseDeliveryNotesService.md#purchasedeliverynotesservice_closebydate)
- [`PurchaseDownPaymentsService_CloseByDate`](../Servicios/PurchaseDownPaymentsService.md#purchasedownpaymentsservice_closebydate)
- [`PurchaseInvoicesService_CloseByDate`](../Servicios/PurchaseInvoicesService.md#purchaseinvoicesservice_closebydate)
- [`PurchaseOrdersService_CloseByDate`](../Servicios/PurchaseOrdersService.md#purchaseordersservice_closebydate)
- [`PurchaseQuotationsService_CloseByDate`](../Servicios/PurchaseQuotationsService.md#purchasequotationsservice_closebydate)
- [`PurchaseRequestService_CloseByDate`](../Servicios/PurchaseRequestService.md#purchaserequestservice_closebydate)
- [`PurchaseReturnsService_CloseByDate`](../Servicios/PurchaseReturnsService.md#purchasereturnsservice_closebydate)
- [`QuotationsService_CloseByDate`](../Servicios/QuotationsService.md#quotationsservice_closebydate)
- [`ReturnRequestService_CloseByDate`](../Servicios/ReturnRequestService.md#returnrequestservice_closebydate)
- [`ReturnsService_CloseByDate`](../Servicios/ReturnsService.md#returnsservice_closebydate)
- [`SelfCreditMemoService_CloseByDate`](../Servicios/SelfCreditMemoService.md#selfcreditmemoservice_closebydate)
- [`SelfInvoiceService_CloseByDate`](../Servicios/SelfInvoiceService.md#selfinvoiceservice_closebydate)
