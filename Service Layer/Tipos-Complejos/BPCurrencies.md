# BPCurrencies — Monedas del socio de negocios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `BPCurrencies`
- **Descripción (ES):** Monedas del socio de negocios
- **Description (EN):** Business Partner Currencies
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 2

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `CurrencyCode` | Edm.String | Yes | Currency Code | Código de moneda |
| 2 | `Include` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Include | Incluir |

## Used by (properties)

- [BusinessPartner](../Entidades/BusinessPartners.md).`BPCurrenciesCollection`
