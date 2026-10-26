# BoStckTrnDir — Dirección de transferencia de stock (servicio)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoStckTrnDir`
- **Descripción (ES):** Dirección de transferencia de stock (servicio)
- **Underlying type:** Edm.Int32
- **Members:** 2

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `bos_TransferToTechnician` | 0 | Transfer To Technician | Transferencia al técnico |
| `bos_TransferFromTechnician` | 1 | Transfer From Technician | Transferencia desde el técnico |

## Used by (1 properties)

- [ServiceCallInventoryExpense](../Tipos-Complejos/ServiceCallInventoryExpense.md).`StockTransferDirection`
