# BPCode — Código del socio de negocios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `BPCode`
- **Descripción (ES):** Código del socio de negocios
- **Description (EN):** Business Partner Code

- **Properties:** 10

## Properties (10)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` | Edm.String | Yes | Code | Código |
| 2 | `DueDate` | Edm.DateTimeOffset | Yes | Due Date | Fecha de vencimiento |
| 3 | `Debit` | Edm.Double | Yes | Debit | Debe/Débito |
| 4 | `Credit` | Edm.Double | Yes | Credit | Haber/Crédito |
| 5 | `SystemDebit` | Edm.Double | Yes | System Debit | Debe (moneda del sistema) |
| 6 | `SystemCredit` | Edm.Double | Yes | System Credit | Haber (moneda del sistema) |
| 7 | `ForeignDebit` | Edm.Double | Yes | Foreign Debit | Debe en moneda extranjera |
| 8 | `ForeignCredit` | Edm.Double | Yes | Foreign Credit | Haber en moneda extranjera |
| 9 | `ForeignCurrency` | Edm.String | Yes | Foreign Currency | Moneda extranjera |
| 10 | `BpCtrlAcct` | Edm.String | Yes | Bp Ctrl Account | Cuenta asociada del socio de negocios |

## Used by (service operations)

- [`BPOpeningBalanceService_CreateOpenBalance`](../Servicios/BPOpeningBalanceService.md#bpopeningbalanceservice_createopenbalance)
- [`BusinessPartnersService_CreateOpenBalance`](../Servicios/BusinessPartnersService.md#businesspartnersservice_createopenbalance)
