# BinRestrictItemEnum — Restricción de artículos en ubicación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BinRestrictItemEnum`
- **Descripción (ES):** Restricción de artículos en ubicación
- **Underlying type:** Edm.Int32
- **Members:** 5

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `briNone` | 0 | None | Ninguna |
| `briSpecificItem` | 1 | Specific Item | Artículo específico |
| `briSingleItemOnly` | 2 | Single Item Only | Solo un artículo |
| `briSpecificItemGroup` | 3 | Specific Item Group | Grupo de artículos específico |
| `briSpecificItemGroupOnly` | 4 | Specific Item Group Only | Solo un grupo de artículos específico |

## Used by (1 properties)

- [BinLocation](../Entidades/BinLocations.md).`RestrictedItemType`
