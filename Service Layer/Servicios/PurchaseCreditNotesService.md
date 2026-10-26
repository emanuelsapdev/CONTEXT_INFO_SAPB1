# PurchaseCreditNotesService — Servicio de notas de crédito de proveedores

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `PurchaseCreditNotesService`
- **Descripción (ES):** Servicio de notas de crédito de proveedores
- **Operations:** 8

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`PurchaseCreditNotesService_ApproveAndAdd`](#purchasecreditnotesservice_approveandadd) | action | — | Approve And Add | Autorizar y agregar |
| [`PurchaseCreditNotesService_ApproveAndUpdate`](#purchasecreditnotesservice_approveandupdate) | action | — | Approve And Update | Autorizar y actualizar |
| [`PurchaseCreditNotesService_Cancel2`](#purchasecreditnotesservice_cancel2) | action | — | Cancel 2 | Cancelar (variante 2) |
| [`PurchaseCreditNotesService_CloseByDate`](#purchasecreditnotesservice_closebydate) | action | — | Close By Date | Cerrar por fecha |
| [`PurchaseCreditNotesService_ExportEWayBill`](#purchasecreditnotesservice_exportewaybill) | action | — | Export E Way Bill | Exportar E-Way Bill |
| [`PurchaseCreditNotesService_GetApprovalTemplates`](#purchasecreditnotesservice_getapprovaltemplates) | action | [Document](../Entidades/PurchaseQuotations.md) | Get Approval Templates | Obtener modelos de autorización |
| [`PurchaseCreditNotesService_HandleApprovalRequest`](#purchasecreditnotesservice_handleapprovalrequest) | action | — | Handle Approval Request | Gestionar solicitud de autorización |
| [`PurchaseCreditNotesService_InitData`](#purchasecreditnotesservice_initdata) | action | [Document](../Entidades/PurchaseQuotations.md) | Init Data | Inicializar datos |

## PurchaseCreditNotesService_ApproveAndAdd

- **Descripción (ES):** Autorizar y agregar
- **Request:** `POST /b1s/v2/PurchaseCreditNotesService_ApproveAndAdd`
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

## PurchaseCreditNotesService_ApproveAndUpdate

- **Descripción (ES):** Autorizar y actualizar
- **Request:** `POST /b1s/v2/PurchaseCreditNotesService_ApproveAndUpdate`
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

## PurchaseCreditNotesService_Cancel2

- **Descripción (ES):** Cancelar (variante 2)
- **Request:** `POST /b1s/v2/PurchaseCreditNotesService_Cancel2`
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

## PurchaseCreditNotesService_CloseByDate

- **Descripción (ES):** Cerrar por fecha
- **Request:** `POST /b1s/v2/PurchaseCreditNotesService_CloseByDate`
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

## PurchaseCreditNotesService_ExportEWayBill

- **Descripción (ES):** Exportar E-Way Bill
- **Request:** `POST /b1s/v2/PurchaseCreditNotesService_ExportEWayBill`
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

## PurchaseCreditNotesService_GetApprovalTemplates

- **Descripción (ES):** Obtener modelos de autorización
- **Request:** `POST /b1s/v2/PurchaseCreditNotesService_GetApprovalTemplates`
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

## PurchaseCreditNotesService_HandleApprovalRequest

- **Descripción (ES):** Gestionar solicitud de autorización
- **Request:** `POST /b1s/v2/PurchaseCreditNotesService_HandleApprovalRequest`
- **Parameters:** none
- **Returns:** nothing (`204 No Content`)

## PurchaseCreditNotesService_InitData

- **Descripción (ES):** Inicializar datos
- **Request:** `POST /b1s/v2/PurchaseCreditNotesService_InitData`
- **Parameters:** none
- **Returns:** [Document](../Entidades/PurchaseQuotations.md)

