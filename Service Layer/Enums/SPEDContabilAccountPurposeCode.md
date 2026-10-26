# SPEDContabilAccountPurposeCode — Código de finalidad de cuenta SPED contable (Brasil)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `SPEDContabilAccountPurposeCode`
- **Descripción (ES):** Código de finalidad de cuenta SPED contable (Brasil)
- **Underlying type:** Edm.Int32
- **Members:** 6

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `spedContasDeAtivo` | 0 | Contas De Ativo | Cuentas de activo |
| `spedContasDePassivo` | 1 | Contas De Passivo | Cuentas de pasivo |
| `spedPatrimonioLiquido` | 2 | Patrimonio Liquido | Patrimonio neto |
| `spedContasDeResultado` | 3 | Contas De Resultado | Cuentas de resultado |
| `spedContasDeCompensacao` | 4 | Contas De Compensacao | Cuentas de compensación |
| `spedOutras` | 5 | Outras | Otras |

## Used by (1 properties)

- [ChartOfAccount](../Entidades/ChartOfAccounts.md).`AccountPurposeCode`
