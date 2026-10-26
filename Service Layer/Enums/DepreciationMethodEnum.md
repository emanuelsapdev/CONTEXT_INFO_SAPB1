# DepreciationMethodEnum — Método de amortización

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `DepreciationMethodEnum`
- **Descripción (ES):** Método de amortización
- **Underlying type:** Edm.Int32
- **Members:** 9

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `dmNoDepreciation` | 0 | Number Depreciation | Sin amortización |
| `dmStraightLine` | 1 | Straight Line | Lineal |
| `dmStraightLinePeriodControl` | 2 | Straight Line Period Control | Lineal con control de período |
| `dmDecliningBalance` | 3 | Declining Balance | Saldo decreciente |
| `dmMultilevel` | 4 | Multilevel | Multinivel |
| `dmImmediateWriteOff` | 5 | Immediate Write Off | Amortización inmediata |
| `dmSpecialDepreciation` | 6 | Special Depreciation | Amortización especial |
| `dmManualDepreciation` | 7 | Manual Depreciation | Amortización manual |
| `dmAccelerated` | 8 | Accelerated | Acelerada |

## Used by (1 properties)

- [DepreciationType](../Entidades/DepreciationTypes.md).`DepreciationMethod`
