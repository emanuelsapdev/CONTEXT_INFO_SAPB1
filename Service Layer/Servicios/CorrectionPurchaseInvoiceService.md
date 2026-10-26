# CorrectionPurchaseInvoiceService — Servicio de facturas de corrección de proveedores

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `CorrectionPurchaseInvoiceService`
- **Descripción (ES):** Servicio de facturas de corrección de proveedores
- **Operations:** 7

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`CorrectionPurchaseInvoiceService_ApproveAndAdd`](#correctionpurchaseinvoiceservice_approveandadd) | action | — | Approve And Add | Autorizar y agregar |
| [`CorrectionPurchaseInvoiceService_ApproveAndUpdate`](#correctionpurchaseinvoiceservice_approveandupdate) | action | — | Approve And Update | Autorizar y actualizar |
| [`CorrectionPurchaseInvoiceService_CloseByDate`](#correctionpurchaseinvoiceservice_closebydate) | action | — | Close By Date | Cerrar por fecha |
| [`CorrectionPurchaseInvoiceService_ExportEWayBill`](#correctionpurchaseinvoiceservice_exportewaybill) | action | — | Export E Way Bill | Exportar E-Way Bill |
| [`CorrectionPurchaseInvoiceService_GetApprovalTemplates`](#correctionpurchaseinvoiceservice_getapprovaltemplates) | action | [Document](../Entidades/PurchaseQuotations.md) | Get Approval Templates | Obtener modelos de autorización |
| [`CorrectionPurchaseInvoiceService_HandleApprovalRequest`](#correctionpurchaseinvoiceservice_handleapprovalrequest) | action | — | Handle Approval Request | Gestionar solicitud de autorización |
| [`CorrectionPurchaseInvoiceService_InitData`](#correctionpurchaseinvoiceservice_initdata) | action | [Document](../Entidades/PurchaseQuotations.md) | Init Data | Inicializar datos |

## CorrectionPurchaseInvoiceService_ApproveAndAdd

- **Descripción (ES):** Autorizar y agregar
- **Request:** `POST /b1s/v2/CorrectionPurchaseInvoiceService_ApproveAndAdd`
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

## CorrectionPurchaseInvoiceService_ApproveAndUpdate

- **Descripción (ES):** Autorizar y actualizar
- **Request:** `POST /b1s/v2/CorrectionPurchaseInvoiceService_ApproveAndUpdate`
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

## CorrectionPurchaseInvoiceService_CloseByDate

- **Descripción (ES):** Cerrar por fecha
- **Request:** `POST /b1s/v2/CorrectionPurchaseInvoiceService_CloseByDate`
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

## CorrectionPurchaseInvoiceService_ExportEWayBill

- **Descripción (ES):** Exportar E-Way Bill
- **Request:** `POST /b1s/v2/CorrectionPurchaseInvoiceService_ExportEWayBill`
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

## CorrectionPurchaseInvoiceService_GetApprovalTemplates

- **Descripción (ES):** Obtener modelos de autorización
- **Request:** `POST /b1s/v2/CorrectionPurchaseInvoiceService_GetApprovalTemplates`
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

## CorrectionPurchaseInvoiceService_HandleApprovalRequest

- **Descripción (ES):** Gestionar solicitud de autorización
- **Request:** `POST /b1s/v2/CorrectionPurchaseInvoiceService_HandleApprovalRequest`
- **Parameters:** none
- **Returns:** nothing (`204 No Content`)

## CorrectionPurchaseInvoiceService_InitData

- **Descripción (ES):** Inicializar datos
- **Request:** `POST /b1s/v2/CorrectionPurchaseInvoiceService_InitData`
- **Parameters:** none
- **Returns:** [Document](../Entidades/PurchaseQuotations.md)

