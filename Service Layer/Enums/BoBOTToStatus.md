# BoBOTToStatus — Estado destino de la transacción de letra de cambio

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoBOTToStatus`
- **Descripción (ES):** Estado destino de la transacción de letra de cambio
- **Underlying type:** Edm.Int32
- **Members:** 6

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `btts_Canceled` | 0 | Canceled | Cancelada |
| `btts_Generated` | 1 | Generated | Generada |
| `btts_Deposit` | 2 | Deposit | Depositada |
| `btts_Paid` | 3 | Paid | Pagada |
| `btts_Failed` | 4 | Failed | Fallida |
| `btts_Closed` | 5 | Closed | Cerrada |

## Used by (1 properties)

- [BillOfExchangeTransaction](../Entidades/BillOfExchangeTransactions.md).`StatusTo`
