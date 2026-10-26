# CurrencyRestriction — Restricción de moneda

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `CurrencyRestriction`
- **Descripción (ES):** Restricción de moneda
- **Description (EN):** Currency Restriction
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `PaymentMethodCode` | Edm.String | Yes | Payment Method Code | Código de vía de pago |
| 2 | `CurrencyCode` | Edm.String | Yes | Currency Code | Código de moneda |
| 3 | `CurrencyName` | Edm.String | Yes | Currency Name | Nombre de la moneda |
| 4 | `Choose` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Choose | Seleccionar |

## Used by (properties)

- [WizardPaymentMethod](../Entidades/WizardPaymentMethods.md).`CurrencyRestrictions`
