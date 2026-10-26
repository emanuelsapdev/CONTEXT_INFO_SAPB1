# TerminationReasonParams — Parámetros de motivos de baja

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `TerminationReasonParams`
- **Descripción (ES):** Parámetros de motivos de baja
- **Description (EN):** Termination Reason Parameters

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ReasonID` | Edm.Int32 | Yes | Reason ID | ID del motivo |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `Description` | Edm.String | Yes | Description | Descripción |

## Used by (service operations)

- [`TerminationReasonService_GetList`](../Servicios/TerminationReasonService.md#terminationreasonservice_getlist)
