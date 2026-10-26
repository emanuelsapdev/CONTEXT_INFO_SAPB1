# BinRestrictionBatchEnum — Restricción de lotes en ubicación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BinRestrictionBatchEnum`
- **Descripción (ES):** Restricción de lotes en ubicación
- **Underlying type:** Edm.Int32
- **Members:** 2

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `brbNoRestrictions` | 0 | Number Restrictions | Sin restricciones |
| `brbSingleBatch` | 1 | Single Batch | Un solo lote |

## Used by (1 properties)

- [BinLocation](../Entidades/BinLocations.md).`BatchRestrictions`
