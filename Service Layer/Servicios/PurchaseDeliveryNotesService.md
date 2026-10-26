# PurchaseDeliveryNotesService — Servicio de pedidos de entrada de mercancías

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `PurchaseDeliveryNotesService`
- **Descripción (ES):** Servicio de pedidos de entrada de mercancías
- **Operations:** 8

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`PurchaseDeliveryNotesService_ApproveAndAdd`](#purchasedeliverynotesservice_approveandadd) | action | — | Approve And Add | Autorizar y agregar |
| [`PurchaseDeliveryNotesService_ApproveAndUpdate`](#purchasedeliverynotesservice_approveandupdate) | action | — | Approve And Update | Autorizar y actualizar |
| [`PurchaseDeliveryNotesService_Cancel2`](#purchasedeliverynotesservice_cancel2) | action | — | Cancel 2 | Cancelar (variante 2) |
| [`PurchaseDeliveryNotesService_CloseByDate`](#purchasedeliverynotesservice_closebydate) | action | — | Close By Date | Cerrar por fecha |
| [`PurchaseDeliveryNotesService_ExportEWayBill`](#purchasedeliverynotesservice_exportewaybill) | action | — | Export E Way Bill | Exportar E-Way Bill |
| [`PurchaseDeliveryNotesService_GetApprovalTemplates`](#purchasedeliverynotesservice_getapprovaltemplates) | action | [Document](../Entidades/PurchaseQuotations.md) | Get Approval Templates | Obtener modelos de autorización |
| [`PurchaseDeliveryNotesService_HandleApprovalRequest`](#purchasedeliverynotesservice_handleapprovalrequest) | action | — | Handle Approval Request | Gestionar solicitud de autorización |
| [`PurchaseDeliveryNotesService_InitData`](#purchasedeliverynotesservice_initdata) | action | [Document](../Entidades/PurchaseQuotations.md) | Init Data | Inicializar datos |

## PurchaseDeliveryNotesService_ApproveAndAdd

- **Descripción (ES):** Autorizar y agregar
- **Request:** `POST /b1s/v2/PurchaseDeliveryNotesService_ApproveAndAdd`
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

## PurchaseDeliveryNotesService_ApproveAndUpdate

- **Descripción (ES):** Autorizar y actualizar
- **Request:** `POST /b1s/v2/PurchaseDeliveryNotesService_ApproveAndUpdate`
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

## PurchaseDeliveryNotesService_Cancel2

- **Descripción (ES):** Cancelar (variante 2)
- **Request:** `POST /b1s/v2/PurchaseDeliveryNotesService_Cancel2`
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

## PurchaseDeliveryNotesService_CloseByDate

- **Descripción (ES):** Cerrar por fecha
- **Request:** `POST /b1s/v2/PurchaseDeliveryNotesService_CloseByDate`
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

## PurchaseDeliveryNotesService_ExportEWayBill

- **Descripción (ES):** Exportar E-Way Bill
- **Request:** `POST /b1s/v2/PurchaseDeliveryNotesService_ExportEWayBill`
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

## PurchaseDeliveryNotesService_GetApprovalTemplates

- **Descripción (ES):** Obtener modelos de autorización
- **Request:** `POST /b1s/v2/PurchaseDeliveryNotesService_GetApprovalTemplates`
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

## PurchaseDeliveryNotesService_HandleApprovalRequest

- **Descripción (ES):** Gestionar solicitud de autorización
- **Request:** `POST /b1s/v2/PurchaseDeliveryNotesService_HandleApprovalRequest`
- **Parameters:** none
- **Returns:** nothing (`204 No Content`)

## PurchaseDeliveryNotesService_InitData

- **Descripción (ES):** Inicializar datos
- **Request:** `POST /b1s/v2/PurchaseDeliveryNotesService_InitData`
- **Parameters:** none
- **Returns:** [Document](../Entidades/PurchaseQuotations.md)

