# TCD5 - Tax Code by Usage

- **Tabla:** TCD5
- **Descripción:** Tax Code by Usage
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TCD5.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Numerator | Int | 11 | - |  |  |
| 2 | `Tcd3Id` | Valid Period ID | Int | 11 | - |  |  |
| 3 | `UsageCode` | Usage | Int | 11 | - |  |  |
| 4 | `TaxCode` | Tax Code | nVarChar | 8 | - |  |  |
| 5 | `Type` | Tax Code Type | VarChar | 1 | - | L | `R` = A/R Default Tax Code<br>`P` = A/P Default Tax Code<br>`L` = Line Item Tax Code |
| 6 | `ExpTaxCode` | Freight Tax Code | nVarChar | 8 | - |  |  |
| 7 | `PurTaxCode` | Purchase Tax Code | nVarChar | 8 | - |  |  |
| 8 | `TcdId` | Tax Determination Code | Int | 11 | - |  |  |
| 9 | `LogInstanc` | Log Instance | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId |
