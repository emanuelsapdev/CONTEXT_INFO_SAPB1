# BoAdEpnsDistribMethods — Método de distribución de gastos adicionales

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoAdEpnsDistribMethods`
- **Descripción (ES):** Método de distribución de gastos adicionales
- **Underlying type:** Edm.Int32
- **Members:** 6

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `aedm_None` | 0 | None | Ninguno |
| `aedm_Quantity` | 1 | Quantity | Cantidad |
| `aedm_Volume` | 2 | Volume | Volumen |
| `aedm_Weight` | 3 | Weight | Peso |
| `aedm_Equally` | 4 | Equally | Partes iguales |
| `aedm_RowTotal` | 5 | Row Total | Total de línea |

## Used by (2 properties)

- [DocumentAdditionalExpense](../Tipos-Complejos/DocumentAdditionalExpense.md).`DistributionMethod`
- [DocumentAdditionalIntrastatExpense](../Tipos-Complejos/DocumentAdditionalIntrastatExpense.md).`DistributionMethod`
