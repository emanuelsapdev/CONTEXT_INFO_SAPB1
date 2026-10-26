# RTM2 - Rate Differences - SC Adjustment Rows

- **Tabla:** RTM2
- **Descripción:** Rate Differences - SC Adjustment Rows
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RTM2.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `LineNum` | Reconciliation Key | Int | 11 | - |  |  |
| 2 | `IsSysCurr` | IS System Currency | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 3 | `CardCode` | BP Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 4 | `AcctCode` | BP Control Account | nVarChar | 15 | - |  |  |
| 5 | `TransAmtSC` | Total Transaction Amount (SC) | Num | 19.6 | - |  |  |
| 6 | `BalDueSC` | Total Balance Due (SC) | Num | 19.6 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | LineNum, IsSysCurr, CardCode, AcctCode |
| CARD_CODE | No | CardCode |
