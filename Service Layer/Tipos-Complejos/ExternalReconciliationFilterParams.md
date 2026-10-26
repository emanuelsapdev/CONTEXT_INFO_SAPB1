# ExternalReconciliationFilterParams — Parámetros de filtro de conciliación externa

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ExternalReconciliationFilterParams`
- **Descripción (ES):** Parámetros de filtro de conciliación externa
- **Description (EN):** External Reconciliation Filter Parameters

- **Properties:** 7

## Properties (7)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AccountCodeFrom` | Edm.String | Yes | Account Code From | Código de cuenta desde |
| 2 | `AccountCodeTo` | Edm.String | Yes | Account Code To | Código de cuenta hasta |
| 3 | `ReconciliationDateFrom` | Edm.DateTimeOffset | Yes | Reconciliation Date From | Fecha de conciliación desde |
| 4 | `ReconciliationDateTo` | Edm.DateTimeOffset | Yes | Reconciliation Date To | Fecha de conciliación hasta |
| 5 | `ReconciliationNoFrom` | Edm.Int32 | Yes | Reconciliation Number From | Número de conciliación desde |
| 6 | `ReconciliationNoTo` | Edm.Int32 | Yes | Reconciliation Number To | Número de conciliación hasta |
| 7 | `ReconciliationAccountType` | [ReconciliationAccountTypeEnum](../Enums/ReconciliationAccountTypeEnum.md) | Yes | Reconciliation Account Type | Tipo de cuenta de conciliación |

## Used by (service operations)

- [`ExternalReconciliationsService_GetReconciliationList`](../Servicios/ExternalReconciliationsService.md#externalreconciliationsservice_getreconciliationlist)
