# AFEFceActionGetPaymentData — [Loc. AR] Datos de pago de la acción FCE

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `AFEFceActionGetPaymentData`
- **Descripción (ES):** [Loc. AR] Datos de pago de la acción FCE
- **Description (EN):** AFE Fce Action Get Payment Data

- **Properties:** 6

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 2 | `CashSum` | Edm.Double | Yes | Cash Sum | Importe en efectivo |
| 3 | `CreditSum` | Edm.Double | Yes | Credit Sum | Importe de tarjeta de crédito |
| 4 | `CheckSum` | Edm.Double | Yes | Check Sum | Importe del cheque |
| 5 | `TrsfrSum` | Edm.Double | Yes | Trsfr Sum | Importe de transferencia |
| 6 | `DocRate` | Edm.Double | Yes | Document Rate | Tipo de cambio del documento |

## Used by (service operations)

- [`ElectronicCommunicationActionService_AFE_FceAction_GetPaymentData`](../Servicios/ElectronicCommunicationActionService.md#electroniccommunicationactionservice_afe_fceaction_getpaymentdata)
