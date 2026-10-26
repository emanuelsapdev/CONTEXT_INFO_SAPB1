# GroupingMethodEnum — Método de agrupación (reclamaciones)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `GroupingMethodEnum`
- **Descripción (ES):** Método de agrupación (reclamaciones)
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `gmPerInvoice` | 0 | Per Invoice | Por factura |
| `gmPerDunningLevel` | 1 | Per Dunning Level | Por nivel de reclamación |
| `gmPerBP` | 2 | Per Business Partner | Por socio de negocios |

## Used by (1 properties)

- [DunningTerm](../Entidades/DunningTerms.md).`GroupingMethod`
