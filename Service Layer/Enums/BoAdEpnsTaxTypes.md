# BoAdEpnsTaxTypes — Tipo de impuesto de gastos adicionales

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoAdEpnsTaxTypes`
- **Descripción (ES):** Tipo de impuesto de gastos adicionales
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `aext_NormalTax` | 0 | Normal Tax | Impuesto normal |
| `aext_NoTax` | 1 | Number Tax | Sin impuesto |
| `aext_UseTax` | 2 | Use Tax | Impuesto de uso |

## Used by (2 properties)

- [DocumentAdditionalExpense](../Tipos-Complejos/DocumentAdditionalExpense.md).`TaxType`
- [DocumentLineAdditionalExpense](../Tipos-Complejos/DocumentLineAdditionalExpense.md).`TaxType`
