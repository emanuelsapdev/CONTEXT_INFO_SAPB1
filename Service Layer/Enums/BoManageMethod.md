# BoManageMethod — Método de gestión de series/lotes

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoManageMethod`
- **Descripción (ES):** Método de gestión de series/lotes
- **Underlying type:** Edm.Int32
- **Members:** 2

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `bomm_OnEveryTransaction` | 0 | On Every Transaction | En cada transacción |
| `bomm_OnReleaseOnly` | 1 | On Release Only | Solo al liberar |

## Used by (2 properties)

- [CompanyInfo](../Tipos-Complejos/CompanyInfo.md).`SRIManagementSystem`
- [Item](../Entidades/Items.md).`SRIAndBatchManageMethod`
