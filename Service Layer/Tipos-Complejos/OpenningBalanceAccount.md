# OpenningBalanceAccount — Cuenta de saldo inicial

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `OpenningBalanceAccount`
- **Descripción (ES):** Cuenta de saldo inicial
- **Description (EN):** Openning Balance Account

- **Properties:** 6

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `OpenBalanceAccount` | Edm.String | Yes | Open Balance Account | Cuenta de saldo inicial |
| 2 | `Date` | Edm.DateTimeOffset | Yes | Date | Fecha |
| 3 | `Ref1` | Edm.String | Yes | Ref 1 | Referencia 1 |
| 4 | `Ref2` | Edm.String | Yes | Ref 2 | Referencia 2 |
| 5 | `Details` | Edm.String | Yes | Details | Detalles |
| 6 | `BPLID` | Edm.Int32 | Yes | BPLID | ID de sucursal |

## Used by (service operations)

- [`AccountsService_CreateOpenBalance`](../Servicios/AccountsService.md#accountsservice_createopenbalance)
- [`BPOpeningBalanceService_CreateOpenBalance`](../Servicios/BPOpeningBalanceService.md#bpopeningbalanceservice_createopenbalance)
- [`BusinessPartnersService_CreateOpenBalance`](../Servicios/BusinessPartnersService.md#businesspartnersservice_createopenbalance)
