# EWBTransactionTypeEnum — Tipo de transacción EWB

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `EWBTransactionTypeEnum`
- **Descripción (ES):** Tipo de transacción EWB
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `ewb_tt_Regular` | 0 | Tt Regular | Regular |
| `ewb_tt_BillToShipTo` | 1 | Tt Bill To Ship To | Facturar a / enviar a |
| `ewb_tt_BillFromDispathFrom` | 2 | Tt Bill From Dispath From | Facturar desde / despachar desde |
| `ewb_tt_CombinationOfBillAndShip` | 3 | Tt Combination Of Bill And Ship | Combinación de facturación y envío |

## Used by (1 properties)

- [EWayBillDetails](../Tipos-Complejos/EWayBillDetails.md).`TransactionType`
