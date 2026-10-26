# BPWithholdingTax — Retención del socio de negocios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `BPWithholdingTax`
- **Descripción (ES):** Retención del socio de negocios
- **Description (EN):** Business Partner Withholding Tax
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 2

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `WTCode` | Edm.String | Yes | Withholding Tax Code | Código de retención |
| 2 | `BPCode` | Edm.String | Yes | Business Partner Code | Código del socio de negocios |

## Used by (properties)

- [BusinessPartner](../Entidades/BusinessPartners.md).`BPWithholdingTaxCollection`
