# ProductionItemType — Tipo de componente de producción

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `ProductionItemType`
- **Descripción (ES):** Tipo de componente de producción
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `pit_Item` | 0 | Item | Artículo |
| `pit_Resource` | 1 | Resource | Recurso |
| `pit_Text` | 2 | Text | Texto |

## Used by (2 properties)

- [ProductTreeLine](../Tipos-Complejos/ProductTreeLine.md).`ItemType`
- [ProductionOrderLine](../Tipos-Complejos/ProductionOrderLine.md).`ItemType`
