# DefaultCreditCard — Tarjetas de crédito predeterminadas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `DefaultCreditCard`
- **Descripción (ES):** Tarjetas de crédito predeterminadas
- **Description (EN):** Default Credit Card
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` | Edm.String | Yes | Code | Código |
| 2 | `CreditAccountCode` | Edm.String | Yes | Credit Account Code | Código de cuenta de haber |
| 3 | `CreditCardCode` | Edm.Int32 | Yes | Credit Card Code | Código de tarjeta de crédito |

## Used by (properties)

- [UserDefaultGroup](../Entidades/UserDefaultGroups.md).`DefaultCreditCards`
