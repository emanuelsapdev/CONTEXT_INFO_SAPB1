# BoAeDistMthd — Método de distribución de gastos adicionales

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoAeDistMthd`
- **Descripción (ES):** Método de distribución de gastos adicionales
- **Underlying type:** Edm.Int32
- **Members:** 6

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `aed_Equally` | 0 | Equally | Partes iguales |
| `aed_LineTotal` | 1 | Line Total | Total de línea |
| `aed_None` | 2 | None | Ninguno |
| `aed_Quantity` | 3 | Quantity | Cantidad |
| `aed_Volume` | 4 | Volume | Volumen |
| `aed_Weight` | 5 | Weight | Peso |

## Used by (1 properties)

- [AdditionalExpense](../Entidades/AdditionalExpenses.md).`DistributionMethod`
