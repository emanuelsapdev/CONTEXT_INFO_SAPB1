# ReturnRequestService — Servicio de solicitudes de devolución

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `ReturnRequestService`
- **Descripción (ES):** Servicio de solicitudes de devolución
- **Operations:** 7

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`ReturnRequestService_ApproveAndAdd`](#returnrequestservice_approveandadd) | action | — | Approve And Add | Autorizar y agregar |
| [`ReturnRequestService_ApproveAndUpdate`](#returnrequestservice_approveandupdate) | action | — | Approve And Update | Autorizar y actualizar |
| [`ReturnRequestService_CloseByDate`](#returnrequestservice_closebydate) | action | — | Close By Date | Cerrar por fecha |
| [`ReturnRequestService_ExportEWayBill`](#returnrequestservice_exportewaybill) | action | — | Export E Way Bill | Exportar E-Way Bill |
| [`ReturnRequestService_GetApprovalTemplates`](#returnrequestservice_getapprovaltemplates) | action | [Document](../Entidades/PurchaseQuotations.md) | Get Approval Templates | Obtener modelos de autorización |
| [`ReturnRequestService_HandleApprovalRequest`](#returnrequestservice_handleapprovalrequest) | action | — | Handle Approval Request | Gestionar solicitud de autorización |
| [`ReturnRequestService_InitData`](#returnrequestservice_initdata) | action | [Document](../Entidades/PurchaseQuotations.md) | Init Data | Inicializar datos |

## ReturnRequestService_ApproveAndAdd

- **Descripción (ES):** Autorizar y agregar
- **Request:** `POST /b1s/v2/ReturnRequestService_ApproveAndAdd`
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

## ReturnRequestService_ApproveAndUpdate

- **Descripción (ES):** Autorizar y actualizar
- **Request:** `POST /b1s/v2/ReturnRequestService_ApproveAndUpdate`
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

## ReturnRequestService_CloseByDate

- **Descripción (ES):** Cerrar por fecha
- **Request:** `POST /b1s/v2/ReturnRequestService_CloseByDate`
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

## ReturnRequestService_ExportEWayBill

- **Descripción (ES):** Exportar E-Way Bill
- **Request:** `POST /b1s/v2/ReturnRequestService_ExportEWayBill`
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

## ReturnRequestService_GetApprovalTemplates

- **Descripción (ES):** Obtener modelos de autorización
- **Request:** `POST /b1s/v2/ReturnRequestService_GetApprovalTemplates`
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

## ReturnRequestService_HandleApprovalRequest

- **Descripción (ES):** Gestionar solicitud de autorización
- **Request:** `POST /b1s/v2/ReturnRequestService_HandleApprovalRequest`
- **Parameters:** none
- **Returns:** nothing (`204 No Content`)

## ReturnRequestService_InitData

- **Descripción (ES):** Inicializar datos
- **Request:** `POST /b1s/v2/ReturnRequestService_InitData`
- **Parameters:** none
- **Returns:** [Document](../Entidades/PurchaseQuotations.md)

