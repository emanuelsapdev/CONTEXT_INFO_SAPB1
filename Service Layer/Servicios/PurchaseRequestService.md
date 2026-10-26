# PurchaseRequestService — Servicio de solicitudes de compra

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `PurchaseRequestService`
- **Descripción (ES):** Servicio de solicitudes de compra
- **Operations:** 7

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`PurchaseRequestService_ApproveAndAdd`](#purchaserequestservice_approveandadd) | action | — | Approve And Add | Autorizar y agregar |
| [`PurchaseRequestService_ApproveAndUpdate`](#purchaserequestservice_approveandupdate) | action | — | Approve And Update | Autorizar y actualizar |
| [`PurchaseRequestService_CloseByDate`](#purchaserequestservice_closebydate) | action | — | Close By Date | Cerrar por fecha |
| [`PurchaseRequestService_ExportEWayBill`](#purchaserequestservice_exportewaybill) | action | — | Export E Way Bill | Exportar E-Way Bill |
| [`PurchaseRequestService_GetApprovalTemplates`](#purchaserequestservice_getapprovaltemplates) | action | [Document](../Entidades/PurchaseQuotations.md) | Get Approval Templates | Obtener modelos de autorización |
| [`PurchaseRequestService_HandleApprovalRequest`](#purchaserequestservice_handleapprovalrequest) | action | — | Handle Approval Request | Gestionar solicitud de autorización |
| [`PurchaseRequestService_InitData`](#purchaserequestservice_initdata) | action | [Document](../Entidades/PurchaseQuotations.md) | Init Data | Inicializar datos |

## PurchaseRequestService_ApproveAndAdd

- **Descripción (ES):** Autorizar y agregar
- **Request:** `POST /b1s/v2/PurchaseRequestService_ApproveAndAdd`
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

## PurchaseRequestService_ApproveAndUpdate

- **Descripción (ES):** Autorizar y actualizar
- **Request:** `POST /b1s/v2/PurchaseRequestService_ApproveAndUpdate`
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

## PurchaseRequestService_CloseByDate

- **Descripción (ES):** Cerrar por fecha
- **Request:** `POST /b1s/v2/PurchaseRequestService_CloseByDate`
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

## PurchaseRequestService_ExportEWayBill

- **Descripción (ES):** Exportar E-Way Bill
- **Request:** `POST /b1s/v2/PurchaseRequestService_ExportEWayBill`
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

## PurchaseRequestService_GetApprovalTemplates

- **Descripción (ES):** Obtener modelos de autorización
- **Request:** `POST /b1s/v2/PurchaseRequestService_GetApprovalTemplates`
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

## PurchaseRequestService_HandleApprovalRequest

- **Descripción (ES):** Gestionar solicitud de autorización
- **Request:** `POST /b1s/v2/PurchaseRequestService_HandleApprovalRequest`
- **Parameters:** none
- **Returns:** nothing (`204 No Content`)

## PurchaseRequestService_InitData

- **Descripción (ES):** Inicializar datos
- **Request:** `POST /b1s/v2/PurchaseRequestService_InitData`
- **Parameters:** none
- **Returns:** [Document](../Entidades/PurchaseQuotations.md)

