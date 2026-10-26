# WTDBP — [Loc. AR] Socio de negocios de la definición de retención

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `WTDBP`
- **Descripción (ES):** [Loc. AR] Socio de negocios de la definición de retención
- **Description (EN):** WTDBP
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 12

## Properties (12)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `BPKeyPart1` | Edm.String | Yes | Business Partner Key Part 1 | Parte 1 de clave del socio de negocios |
| 2 | `BPKeyPart2` | Edm.String | Yes | Business Partner Key Part 2 | Parte 2 de clave del socio de negocios |
| 3 | `WTaxCode` | Edm.String | Yes | W Tax Code | Código de retención |
| 4 | `EffectiveDateFrom` | Edm.DateTimeOffset | Yes | Effective Date From | Fecha de vigencia desde |
| 5 | `EffectiveDateTo` | Edm.DateTimeOffset | Yes | Effective Date To | Fecha de vigencia hasta |
| 6 | `Rate` | Edm.Double | Yes | Rate | Tasa / tipo de cambio |
| 7 | `DetailType` | [WTDDetailType](../Enums/WTDDetailType.md) | Yes | Detail Type | Tipo de detalle |
| 8 | `U_B1SYS_HighRisk` | Edm.String | Yes | [AR localization] High Risk | [Loc. AR] Contribuyente de alto riesgo fiscal |
| 9 | `U_B1SYS_Reason` | Edm.String | Yes | [AR localization] Reason | [Loc. AR] Motivo |
| 10 | `U_B1SYS_ExemptID` | Edm.String | Yes | [AR localization] Exempt ID | [Loc. AR] ID de exención |
| 11 | `U_B1SYS_CheckDate` | Edm.DateTimeOffset | Yes | [AR localization] Check Date | [Loc. AR] Fecha de verificación |
| 12 | `U_B1SYS_CheckSetByPd` | Edm.String | Yes | [AR localization] Check Set By Pd | [Loc. AR] Verificado por padrón |

## Used by (properties)

- [WTDCode](../Entidades/WitholdingTaxDefinition.md).`WTDBPCollection`
