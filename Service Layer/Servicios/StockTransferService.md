# StockTransferService — Servicio de transferencias de stock

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `StockTransferService`
- **Descripción (ES):** Servicio de transferencias de stock
- **Operations:** 2

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`StockTransferService_GetApprovalTemplates`](#stocktransferservice_getapprovaltemplates) | action | [StockTransfer](../Entidades/StockTransfers.md) | Get Approval Templates | Obtener modelos de autorización |
| [`StockTransferService_HandleApprovalRequest`](#stocktransferservice_handleapprovalrequest) | action | — | Handle Approval Request | Gestionar solicitud de autorización |

## StockTransferService_GetApprovalTemplates

- **Descripción (ES):** Obtener modelos de autorización
- **Request:** `POST /b1s/v2/StockTransferService_GetApprovalTemplates`
- **Parameters:** `StockTransfer` ([StockTransfer](../Entidades/StockTransfers.md))
- **Returns:** [StockTransfer](../Entidades/StockTransfers.md)

```json
{
  "StockTransfer": {
    "DocEntry": 0,
    "Series": 0,
    "DocDate": "2026-01-31",
    "DueDate": "2026-01-31",
    ...
  }
}
```

## StockTransferService_HandleApprovalRequest

- **Descripción (ES):** Gestionar solicitud de autorización
- **Request:** `POST /b1s/v2/StockTransferService_HandleApprovalRequest`
- **Parameters:** none
- **Returns:** nothing (`204 No Content`)

