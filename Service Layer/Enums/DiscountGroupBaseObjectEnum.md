# DiscountGroupBaseObjectEnum — Objeto base del grupo de descuento

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `DiscountGroupBaseObjectEnum`
- **Descripción (ES):** Objeto base del grupo de descuento
- **Underlying type:** Edm.Int32
- **Members:** 5

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `dgboNone` | 0 | None | Ninguno |
| `dgboItemGroups` | 1 | Item Groups | Grupos de artículos |
| `dgboItemProperties` | 2 | Item Properties | Propiedades de artículos |
| `dgboManufacturer` | 3 | Manufacturer | Fabricante |
| `dgboItems` | 4 | Items | Artículos |

## Used by (3 properties)

- [BusinessPartner](../Entidades/BusinessPartners.md).`DiscountBaseObject`
- [DiscountGroup](../Tipos-Complejos/DiscountGroup.md).`BaseObjectType`
- [DiscountGroupLine](../Tipos-Complejos/DiscountGroupLine.md).`ObjectType`
