# BPAccountReceivablePayble — Cuenta asociada por cobrar/pagar del socio de negocios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `BPAccountReceivablePayble`
- **Descripción (ES):** Cuenta asociada por cobrar/pagar del socio de negocios
- **Description (EN):** Business Partner Account Receivable Payble
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AccountType` | [BoBpAccountTypes](../Enums/BoBpAccountTypes.md) | Yes | Account Type | Tipo de cuenta |
| 2 | `AccountCode` | Edm.String | Yes | Account Code | Código de cuenta |
| 3 | `BPCode` | Edm.String | Yes | Business Partner Code | Código del socio de negocios |

## Used by (properties)

- [BusinessPartner](../Entidades/BusinessPartners.md).`BPAccountReceivablePaybleCollection`
