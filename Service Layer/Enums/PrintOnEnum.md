# PrintOnEnum — Imprimir en

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `PrintOnEnum`
- **Descripción (ES):** Imprimir en
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `poBlankPaper` | 0 | Blank Paper | Papel en blanco |
| `poDefault` | 1 | Default | Predeterminado |
| `poOverflowBlankPaper` | 2 | Overflow Blank Paper | Desbordamiento en papel en blanco |
| `poOverflowCheckStock` | 3 | Overflow Check Stock | Desbordamiento en formulario de cheque |

## Used by (1 properties)

- [HouseBankAccount](../Entidades/HouseBankAccounts.md).`PrintOn`
