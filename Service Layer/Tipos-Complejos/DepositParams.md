# DepositParams — Parámetros de depósitos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `DepositParams`
- **Descripción (ES):** Parámetros de depósitos
- **Description (EN):** Deposit Parameters

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DepositNumber` | Edm.Int32 | Yes | Deposit Number | Número de depósito |
| 2 | `AbsEntry` | Edm.Int32 | Yes | Abs Entry | Entrada absoluta (ID interno) |
| 3 | `Series` | Edm.Int32 | Yes | Series | Serie de numeración |

## Used by (service operations)

- [`DepositsService_GetDepositList`](../Servicios/DepositsService.md#depositsservice_getdepositlist)
