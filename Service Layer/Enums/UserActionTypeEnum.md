# UserActionTypeEnum — Tipo de acción del usuario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `UserActionTypeEnum`
- **Descripción (ES):** Tipo de acción del usuario
- **Underlying type:** Edm.Int32
- **Members:** 11

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `actionLogin` | 0 | Login | Inicio de sesión |
| `actionLoginFail` | 1 | Login Fail | Inicio de sesión fallido |
| `actionLogoff` | 2 | Logoff | Cierre de sesión |
| `actionCreateUser` | 3 | Create User | Creación de usuario |
| `actionRemoveUser` | 4 | Remove User | Eliminación de usuario |
| `actionSelectSU` | 5 | Select SU | Asignar superusuario |
| `actionDeselectSU` | 6 | Deselect SU | Quitar superusuario |
| `actionLock` | 7 | Lock | Bloqueo |
| `actionUnlock` | 8 | Unlock | Desbloqueo |
| `actionChPasswd` | 9 | Ch Passwd | Cambio de contraseña |
| `actionUnlockFail` | 10 | Unlock Fail | Desbloqueo fallido |

## Used by (2 properties)

- [UserAccessLog](../Tipos-Complejos/UserAccessLog.md).`Action`
- [UserActionRecordItem](../Tipos-Complejos/UserActionRecordItem.md).`Action`
