# ActivityRecipientListParams — Parámetros de listas de destinatarios de actividades

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ActivityRecipientListParams`
- **Descripción (ES):** Parámetros de listas de destinatarios de actividades
- **Description (EN):** Activity Recipient List Parameters

- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` | Edm.Int32 | Yes | Code | Código |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `Active` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Active | Activo |
| 4 | `IsMultiple` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Multiple | Es múltiple |

## Used by (service operations)

- [`ActivityRecipientListsService_GetList`](../Servicios/ActivityRecipientListsService.md#activityrecipientlistsservice_getlist)
