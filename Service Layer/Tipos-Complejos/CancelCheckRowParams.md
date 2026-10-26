# CancelCheckRowParams — Parámetros de cancelación de línea de cheque

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `CancelCheckRowParams`
- **Descripción (ES):** Parámetros de cancelación de línea de cheque
- **Description (EN):** Cancel Check Row Parameters

- **Properties:** 2

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DepositID` | Edm.Int32 | Yes | Deposit ID | ID del depósito |
| 2 | `CheckID` | Edm.Int32 | Yes | Check ID | ID del cheque |

## Used by (service operations)

- [`DepositsService_CancelCheckRow`](../Servicios/DepositsService.md#depositsservice_cancelcheckrow)
- [`DepositsService_CancelCheckRowbyCurrentSystemDate`](../Servicios/DepositsService.md#depositsservice_cancelcheckrowbycurrentsystemdate)
