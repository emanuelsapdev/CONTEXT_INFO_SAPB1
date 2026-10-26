# BillOfExchangeTransactionLine — Líneas de transacción de letras de cambio

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `BillOfExchangeTransactionLine`
- **Descripción (ES):** Líneas de transacción de letras de cambio
- **Description (EN):** Bill Of Exchange Transaction Line
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `BillOfExchangeNo` | Edm.Int32 | Yes | Bill Of Exchange Number | Número de letra de cambio |
| 2 | `BillOfExchangeType` | [BoBOETypes](../Enums/BoBOETypes.md) | Yes | Bill Of Exchange Type | Tipo de letra de cambio |
| 3 | `BillOfExchangeDueDate` | Edm.DateTimeOffset | Yes | Bill Of Exchange Due Date | Fecha de vencimiento de letra de cambio |

## Used by (properties)

- [BillOfExchangeTransaction](../Entidades/BillOfExchangeTransactions.md).`BillOfExchangeTransactionLines`
