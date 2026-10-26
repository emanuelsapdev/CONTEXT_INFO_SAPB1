# BinRestrictUoMEnum — Restricción de unidades de medida en ubicación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BinRestrictUoMEnum`
- **Descripción (ES):** Restricción de unidades de medida en ubicación
- **Underlying type:** Edm.Int32
- **Members:** 5

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `bruNone` | 0 | None | Ninguna |
| `bruSpecificUoM` | 1 | Specific Uo M | Unidad de medida específica |
| `bruSingleUoMOnly` | 2 | Single Uo M Only | Solo una unidad de medida |
| `bruSpecificUoMGroup` | 3 | Specific Uo M Group | Grupo de unidades de medida específico |
| `bruSpecificUoMGroupOnly` | 4 | Specific Uo M Group Only | Solo un grupo de unidades de medida |

## Used by (1 properties)

- [BinLocation](../Entidades/BinLocations.md).`RestrictedUoMType`
