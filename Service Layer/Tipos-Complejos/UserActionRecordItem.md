# UserActionRecordItem — Registro de acción del usuario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `UserActionRecordItem`
- **Descripción (ES):** Registro de acción del usuario
- **Description (EN):** User Action Record Item
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 12

## Properties (12)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `UserCode` | Edm.String | Yes | User Code | Código de usuario |
| 2 | `Action` | [UserActionTypeEnum](../Enums/UserActionTypeEnum.md) | Yes | Action | Acción |
| 3 | `ActionBy` | Edm.String | Yes | Action By | Acción realizada por |
| 4 | `ClientIP` | Edm.String | Yes | Client IP | IP del cliente |
| 5 | `ClientName` | Edm.String | Yes | Client Name | Nombre del cliente |
| 6 | `ActionDate` | Edm.DateTimeOffset | Yes | Action Date | Fecha de la acción |
| 7 | `ActionTime` | Edm.TimeOfDay | Yes | Action Time | Hora de la acción |
| 8 | `WindowsSession` | Edm.Int32 | Yes | Windows Session | Sesión de Windows |
| 9 | `WindowsUser` | Edm.String | Yes | Windows User | Usuario de Windows |
| 10 | `ProcessName` | Edm.String | Yes | Process Name | Nombre del proceso |
| 11 | `ProcessID` | Edm.Int32 | Yes | Process ID | ID de proceso |
| 12 | `AliveDuration` | Edm.Int32 | Yes | Alive Duration | Duración activa |

## Used by (properties)

- [User](../Entidades/Users.md).`UserActionRecord`
