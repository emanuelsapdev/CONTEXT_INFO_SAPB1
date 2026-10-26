# ReconSelectDateTypeEnum — Tipo de fecha para conciliación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `ReconSelectDateTypeEnum`
- **Descripción (ES):** Tipo de fecha para conciliación
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `rsdtPostDate` | 0 | Post Date | Fecha de contabilización |
| `rsdtDueDate` | 1 | Due Date | Fecha de vencimiento |
| `rsdtDocDate` | 2 | Document Date | Fecha del documento |

## Used by (1 properties)

- [InternalReconciliationOpenTransParams](../Tipos-Complejos/InternalReconciliationOpenTransParams.md).`DateType`
