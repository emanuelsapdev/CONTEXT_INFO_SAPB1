# BoBOTFromStatus — Estado origen de la transacción de letra de cambio

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoBOTFromStatus`
- **Descripción (ES):** Estado origen de la transacción de letra de cambio
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `btfs_Sent` | 0 | Sent | Enviada |
| `btfs_Generated` | 1 | Generated | Generada |
| `btfs_Deposited` | 2 | Deposited | Depositada |
| `btfs_Paid` | 3 | Paid | Pagada |

## Used by (1 properties)

- [BillOfExchangeTransaction](../Entidades/BillOfExchangeTransactions.md).`StatusFrom`
