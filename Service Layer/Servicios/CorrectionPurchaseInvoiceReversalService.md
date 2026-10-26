# CorrectionPurchaseInvoiceReversalService — Servicio de anulación de facturas de corrección de proveedores

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `CorrectionPurchaseInvoiceReversalService`
- **Descripción (ES):** Servicio de anulación de facturas de corrección de proveedores
- **Operations:** 7

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`CorrectionPurchaseInvoiceReversalService_ApproveAndAdd`](#correctionpurchaseinvoicereversalservice_approveandadd) | action | — | Approve And Add | Autorizar y agregar |
| [`CorrectionPurchaseInvoiceReversalService_ApproveAndUpdate`](#correctionpurchaseinvoicereversalservice_approveandupdate) | action | — | Approve And Update | Autorizar y actualizar |
| [`CorrectionPurchaseInvoiceReversalService_CloseByDate`](#correctionpurchaseinvoicereversalservice_closebydate) | action | — | Close By Date | Cerrar por fecha |
| [`CorrectionPurchaseInvoiceReversalService_ExportEWayBill`](#correctionpurchaseinvoicereversalservice_exportewaybill) | action | — | Export E Way Bill | Exportar E-Way Bill |
| [`CorrectionPurchaseInvoiceReversalService_GetApprovalTemplates`](#correctionpurchaseinvoicereversalservice_getapprovaltemplates) | action | [Document](../Entidades/PurchaseQuotations.md) | Get Approval Templates | Obtener modelos de autorización |
| [`CorrectionPurchaseInvoiceReversalService_HandleApprovalRequest`](#correctionpurchaseinvoicereversalservice_handleapprovalrequest) | action | — | Handle Approval Request | Gestionar solicitud de autorización |
| [`CorrectionPurchaseInvoiceReversalService_InitData`](#correctionpurchaseinvoicereversalservice_initdata) | action | [Document](../Entidades/PurchaseQuotations.md) | Init Data | Inicializar datos |

## CorrectionPurchaseInvoiceReversalService_ApproveAndAdd

- **Descripción (ES):** Autorizar y agregar
- **Request:** `POST /b1s/v2/CorrectionPurchaseInvoiceReversalService_ApproveAndAdd`
- **Parameters:** `Document` ([Document](../Entidades/PurchaseQuotations.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "Document": {
    "DocEntry": 0,
    "DocNum": 0,
    "DocDate": "2026-01-31",
    "DocDueDate": "2026-01-31",
    ...
  }
}
```

## CorrectionPurchaseInvoiceReversalService_ApproveAndUpdate

- **Descripción (ES):** Autorizar y actualizar
- **Request:** `POST /b1s/v2/CorrectionPurchaseInvoiceReversalService_ApproveAndUpdate`
- **Parameters:** `Document` ([Document](../Entidades/PurchaseQuotations.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "Document": {
    "DocEntry": 0,
    "DocNum": 0,
    "DocDate": "2026-01-31",
    "DocDueDate": "2026-01-31",
    ...
  }
}
```

## CorrectionPurchaseInvoiceReversalService_CloseByDate

- **Descripción (ES):** Cerrar por fecha
- **Request:** `POST /b1s/v2/CorrectionPurchaseInvoiceReversalService_CloseByDate`
- **Parameters:** `DocumentCloseParams` ([DocumentCloseParams](../Tipos-Complejos/DocumentCloseParams.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "DocumentCloseParams": {
    "DocEntry": 0,
    "SpecifiedClosingDate": "2026-01-31",
    ...
  }
}
```

## CorrectionPurchaseInvoiceReversalService_ExportEWayBill

- **Descripción (ES):** Exportar E-Way Bill
- **Request:** `POST /b1s/v2/CorrectionPurchaseInvoiceReversalService_ExportEWayBill`
- **Parameters:** `Document` ([Document](../Entidades/PurchaseQuotations.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "Document": {
    "DocEntry": 0,
    "DocNum": 0,
    "DocDate": "2026-01-31",
    "DocDueDate": "2026-01-31",
    ...
  }
}
```

## CorrectionPurchaseInvoiceReversalService_GetApprovalTemplates

- **Descripción (ES):** Obtener modelos de autorización
- **Request:** `POST /b1s/v2/CorrectionPurchaseInvoiceReversalService_GetApprovalTemplates`
- **Parameters:** `Document` ([Document](../Entidades/PurchaseQuotations.md))
- **Returns:** [Document](../Entidades/PurchaseQuotations.md)

```json
{
  "Document": {
    "DocEntry": 0,
    "DocNum": 0,
    "DocDate": "2026-01-31",
    "DocDueDate": "2026-01-31",
    ...
  }
}
```

## CorrectionPurchaseInvoiceReversalService_HandleApprovalRequest

- **Descripción (ES):** Gestionar solicitud de autorización
- **Request:** `POST /b1s/v2/CorrectionPurchaseInvoiceReversalService_HandleApprovalRequest`
- **Parameters:** none
- **Returns:** nothing (`204 No Content`)

## CorrectionPurchaseInvoiceReversalService_InitData

- **Descripción (ES):** Inicializar datos
- **Request:** `POST /b1s/v2/CorrectionPurchaseInvoiceReversalService_InitData`
- **Parameters:** none
- **Returns:** [Document](../Entidades/PurchaseQuotations.md)

