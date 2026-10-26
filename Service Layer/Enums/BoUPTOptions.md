# BoUPTOptions — Opciones de autorización de usuario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoUPTOptions`
- **Descripción (ES):** Opciones de autorización de usuario
- **Underlying type:** Edm.Int32
- **Members:** 2

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `bou_FullNone` | 0 | Full None | Total/ninguna |
| `bou_FullReadNone` | 1 | Full Read None | Total/solo lectura/ninguna |

## Used by (1 properties)

- [UserPermissionTree](../Entidades/UserPermissionTree.md).`Options`
