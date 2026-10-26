# ExternalReconciliationParams — Parámetros de conciliación externa

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ExternalReconciliationParams`
- **Descripción (ES):** Parámetros de conciliación externa
- **Description (EN):** External Reconciliation Parameters

- **Properties:** 2

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AccountCode` | Edm.String | Yes | Account Code | Código de cuenta |
| 2 | `ReconciliationNo` | Edm.Int32 | Yes | Reconciliation Number | Número de conciliación |

## Used by (service operations)

- [`ExternalReconciliationsService_CancelReconciliation`](../Servicios/ExternalReconciliationsService.md#externalreconciliationsservice_cancelreconciliation)
- [`ExternalReconciliationsService_GetReconciliation`](../Servicios/ExternalReconciliationsService.md#externalreconciliationsservice_getreconciliation)
- [`ExternalReconciliationsService_GetReconciliationList`](../Servicios/ExternalReconciliationsService.md#externalreconciliationsservice_getreconciliationlist)
