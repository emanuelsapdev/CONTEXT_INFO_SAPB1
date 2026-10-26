# UserMenuItem — Elemento de menú de usuario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `UserMenuItem`
- **Descripción (ES):** Elemento de menú de usuario
- **Description (EN):** User Menu Item

- **Properties:** 8

## Properties (8)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Name` | Edm.String | Yes | Name | Nombre |
| 2 | `Position` | Edm.Int32 | Yes | Position | Posición/cargo |
| 3 | `Type` | [UserMenuItemTypeEnum](../Enums/UserMenuItemTypeEnum.md) | Yes | Type | Tipo |
| 4 | `LinkedObjType` | Edm.String | Yes | Linked Obj Type | Tipo de objeto vinculado |
| 5 | `LinkedObjKey` | Edm.String | Yes | Linked Obj Key | Clave del objeto vinculado |
| 6 | `LinkedFormMenuID` | Edm.Int32 | Yes | Linked Form Menu ID | ID de menú del formulario vinculado |
| 7 | `LinkedFormNum` | Edm.Int32 | Yes | Linked Form Number | Número de formulario vinculado |
| 8 | `ReportPath` | Edm.String | Yes | Report Path | Ruta del informe |

## Used by (service operations)

- [`UserMenuService_GetCurrentUserMenu`](../Servicios/UserMenuService.md#usermenuservice_getcurrentusermenu)
- [`UserMenuService_GetUserMenu`](../Servicios/UserMenuService.md#usermenuservice_getusermenu)
- [`UserMenuService_UpdateCurrentUserMenu`](../Servicios/UserMenuService.md#usermenuservice_updatecurrentusermenu)
- [`UserMenuService_UpdateUserMenu`](../Servicios/UserMenuService.md#usermenuservice_updateusermenu)
