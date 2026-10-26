# GetGLAccountByEnum — Obtener cuenta de mayor por

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `GetGLAccountByEnum`
- **Descripción (ES):** Obtener cuenta de mayor por
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `gglab_General` | 0 | General | General |
| `gglab_Warehouse` | 1 | Warehouse | Almacén |
| `gglab_ItemGroup` | 2 | Item Group | Grupo de artículos |

## Used by (1 properties)

- [GLAccountAdvancedRule](../Entidades/GLAccountAdvancedRules.md).`GetGLAccountBy`
