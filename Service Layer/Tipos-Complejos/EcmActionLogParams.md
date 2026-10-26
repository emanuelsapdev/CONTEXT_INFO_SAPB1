# EcmActionLogParams — Parámetros de registro de acción ECM

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `EcmActionLogParams`
- **Descripción (ES):** Parámetros de registro de acción ECM
- **Description (EN):** Ecm Action Log Parameters

- **Properties:** 2

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ActionID` | Edm.Int32 | Yes | Action ID | ID de acción |
| 2 | `LogID` | Edm.Int32 | Yes | Log ID | ID de registro |

## Used by (service operations)

- [`ElectronicCommunicationActionsService_GetEcmActionLog`](../Servicios/ElectronicCommunicationActionsService.md#electroniccommunicationactionsservice_getecmactionlog)
