# PurchaseQuotationsService — Servicio de ofertas de compra

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `PurchaseQuotationsService`
- **Descripción (ES):** Servicio de ofertas de compra
- **Operations:** 7

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`PurchaseQuotationsService_ApproveAndAdd`](#purchasequotationsservice_approveandadd) | action | — | Approve And Add | Autorizar y agregar |
| [`PurchaseQuotationsService_ApproveAndUpdate`](#purchasequotationsservice_approveandupdate) | action | — | Approve And Update | Autorizar y actualizar |
| [`PurchaseQuotationsService_CloseByDate`](#purchasequotationsservice_closebydate) | action | — | Close By Date | Cerrar por fecha |
| [`PurchaseQuotationsService_ExportEWayBill`](#purchasequotationsservice_exportewaybill) | action | — | Export E Way Bill | Exportar E-Way Bill |
| [`PurchaseQuotationsService_GetApprovalTemplates`](#purchasequotationsservice_getapprovaltemplates) | action | [Document](../Entidades/PurchaseQuotations.md) | Get Approval Templates | Obtener modelos de autorización |
| [`PurchaseQuotationsService_HandleApprovalRequest`](#purchasequotationsservice_handleapprovalrequest) | action | — | Handle Approval Request | Gestionar solicitud de autorización |
| [`PurchaseQuotationsService_InitData`](#purchasequotationsservice_initdata) | action | [Document](../Entidades/PurchaseQuotations.md) | Init Data | Inicializar datos |

## PurchaseQuotationsService_ApproveAndAdd

- **Descripción (ES):** Autorizar y agregar
- **Request:** `POST /b1s/v2/PurchaseQuotationsService_ApproveAndAdd`
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

## PurchaseQuotationsService_ApproveAndUpdate

- **Descripción (ES):** Autorizar y actualizar
- **Request:** `POST /b1s/v2/PurchaseQuotationsService_ApproveAndUpdate`
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

## PurchaseQuotationsService_CloseByDate

- **Descripción (ES):** Cerrar por fecha
- **Request:** `POST /b1s/v2/PurchaseQuotationsService_CloseByDate`
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

## PurchaseQuotationsService_ExportEWayBill

- **Descripción (ES):** Exportar E-Way Bill
- **Request:** `POST /b1s/v2/PurchaseQuotationsService_ExportEWayBill`
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

## PurchaseQuotationsService_GetApprovalTemplates

- **Descripción (ES):** Obtener modelos de autorización
- **Request:** `POST /b1s/v2/PurchaseQuotationsService_GetApprovalTemplates`
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

## PurchaseQuotationsService_HandleApprovalRequest

- **Descripción (ES):** Gestionar solicitud de autorización
- **Request:** `POST /b1s/v2/PurchaseQuotationsService_HandleApprovalRequest`
- **Parameters:** none
- **Returns:** nothing (`204 No Content`)

## PurchaseQuotationsService_InitData

- **Descripción (ES):** Inicializar datos
- **Request:** `POST /b1s/v2/PurchaseQuotationsService_InitData`
- **Parameters:** none
- **Returns:** [Document](../Entidades/PurchaseQuotations.md)

