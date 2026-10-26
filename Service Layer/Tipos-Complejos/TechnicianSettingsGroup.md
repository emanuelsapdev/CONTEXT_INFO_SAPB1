# TechnicianSettingsGroup — Grupo de configuración de técnicos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `TechnicianSettingsGroup`
- **Descripción (ES):** Grupo de configuración de técnicos
- **Description (EN):** Technician Settings Group

- **Properties:** 11

## Properties (11)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` | Edm.Int32 | Yes | Code | Código |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `CustomizedGroup` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Customized Group | Grupo personalizado |
| 4 | `EnableEditTime` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enable Edit Time | Habilitar edición de hora |
| 5 | `EnableReject` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enable Reject | Habilitar rechazo |
| 6 | `EnableResign` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enable Resign | Habilitar renuncia |
| 7 | `EnableFollowup` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enable Followup | Habilitar seguimiento |
| 8 | `EnableSignature` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enable Signature | Habilitar firma |
| 9 | `EnableStarRating` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enable Star Rating | Habilitar calificación por estrellas |
| 10 | `EnableActualDuration` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enable Actual Duration | Habilitar duración real |
| 11 | `AdvancedDashBoard` | Edm.Int32 | Yes | Advanced Dash Board | Dashboard avanzado |

## Used by (service operations)

- [`MobileAppService_GetTechnicianSettingsGroup`](../Servicios/MobileAppService.md#mobileappservice_gettechniciansettingsgroup)
- [`MobileAppService_UpdateTechnicianSettingsGroup`](../Servicios/MobileAppService.md#mobileappservice_updatetechniciansettingsgroup)
