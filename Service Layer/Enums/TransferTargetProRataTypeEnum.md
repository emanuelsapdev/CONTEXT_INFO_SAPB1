# TransferTargetProRataTypeEnum — Tipo de prorrata del destino de transferencia

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `TransferTargetProRataTypeEnum`
- **Descripción (ES):** Tipo de prorrata del destino de transferencia
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `ttprtExactlyDailyBase` | 0 | Exactly Daily Base | Base diaria exacta |
| `ttprtFirstDayOfCurrentPeriod` | 1 | First Day Of Current Period | Primer día del período actual |
| `ttprtFirstDayOfNextPeriod` | 2 | First Day Of Next Period | Primer día del período siguiente |

## Used by (1 properties)

- [DepreciationType](../Entidades/DepreciationTypes.md).`TransferTargetProRataType`
