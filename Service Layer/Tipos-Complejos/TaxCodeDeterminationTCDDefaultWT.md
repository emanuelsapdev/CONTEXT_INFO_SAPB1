# TaxCodeDeterminationTCDDefaultWT — Retenciones predeterminadas de la determinación TCD

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `TaxCodeDeterminationTCDDefaultWT`
- **Descripción (ES):** Retenciones predeterminadas de la determinación TCD
- **Description (EN):** Tax Code Determination TCD Default Withholding Tax

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsId` | Edm.Int32 | Yes | Abs ID | ID absoluto |
| 2 | `WTCode` | Edm.String | Yes | Withholding Tax Code | Código de retención |
| 3 | `Type` | [TaxCodeDeterminationTCDDefaultWTTypeEnum](../Enums/TaxCodeDeterminationTCDDefaultWTTypeEnum.md) | Yes | Type | Tipo |

## Used by (properties)

- [TaxCodeDeterminationTCD](../Entidades/TaxCodeDeterminationsTCD.md).`TaxCodeDeterminationTCDDefaultWTs`
