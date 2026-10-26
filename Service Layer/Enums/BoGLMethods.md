# BoGLMethods — Método de cuentas de mayor del artículo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoGLMethods`
- **Descripción (ES):** Método de cuentas de mayor del artículo
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `glm_WH` | 0 | Warehouse | Por almacén |
| `glm_ItemClass` | 1 | Item Class | Por grupo de artículos |
| `glm_ItemLevel` | 2 | Item Level | Por artículo |

## Used by (2 properties)

- [AdminInfo](../Tipos-Complejos/AdminInfo.md).`GLMethod`
- [Item](../Entidades/Items.md).`GLMethod`
