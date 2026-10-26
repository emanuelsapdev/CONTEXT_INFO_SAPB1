# BoPermission — Nivel de autorización

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoPermission`
- **Descripción (ES):** Nivel de autorización
- **Underlying type:** Edm.Int32
- **Members:** 5

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `boper_Full` | 1 | Full | Total |
| `boper_ReadOnly` | 2 | Read Only | Solo lectura |
| `boper_None` | 3 | None | Sin autorización |
| `boper_Various` | 4 | Various | Varios |
| `boper_Undefined` | 6 | Undefined | Indefinido |

## Used by (2 properties)

- [UserPermissionItem](../Tipos-Complejos/UserPermissionItem.md).`EffectivePermission`
- [UserPermissionItem](../Tipos-Complejos/UserPermissionItem.md).`Permission`
