# OMTC - Bank Statement - Matching Criteria

- **Tabla:** OMTC
- **Descripción:** Bank Statement - Matching Criteria
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OMTC.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `MatchID` | Form Type Index | Int | 6 | - | 1 | `1` = Documents<br>`2` = Internal Reconciliation<br>`3` = External Reconciliation |
| 3 | `Round` | Rounding | Int | 6 | - |  | `1` = Round 1<br>`2` = Round 2<br>`3` = Round 3 |
| 4 | `MtcRule` | Matching Rule | Int | 6 | - | 0 |  |
| 5 | `MtcAlias` | Matching Alias | nVarChar | 50 | - |  |  |
| 6 | `Differnce` | Difference | Int | 11 | - | 0 |  |
| 7 | `DiffAmnt` | Amount Difference | Num | 19.6 | - |  |  |
| 8 | `RuleIndex` | Rule Index | Int | 6 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry |
| MATCH_TYPE | Yes | MatchID, Round, RuleIndex |
