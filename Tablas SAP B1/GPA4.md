# GPA4 - Gross Profit Adjustment - JE Details Accounts

- **Tabla:** GPA4
- **Descripción:** Gross Profit Adjustment - JE Details Accounts
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/GPA4.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | [OGPA](OGPA.md) |  |  |
| 2 | `LineId` | Row No. | Int | 11 | - |  |  |
| 3 | `LineType` | Line Type | VarChar | 1 | - | T | `T` = Total<br>`A` = Account |
| 4 | `CurrCogs` | Current COGS | Num | 19.6 | - |  |  |
| 5 | `CalcCogs` | Calculated COGS | Num | 19.6 | - |  |  |
| 6 | `CogsDebit` | COGS Debit | Num | 19.6 | - |  |  |
| 7 | `CogsCredit` | COGS Credit | Num | 19.6 | - |  |  |
| 8 | `CogsAcct` | COGS Account | nVarChar | 15 | - |  |  |
| 9 | `PrDiffAcct` | Price Difference Account | nVarChar | 15 | - |  |  |
| 10 | `AutoPost` | Automatic Posting | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineId |
