# DUT1 - Dunning Term Array1

- **Tabla:** DUT1
- **Descripción:** Dunning Term Array1
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/DUT1.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TermCode` | Dunning Term Code | nVarChar | 25 | [ODUT](ODUT.md) |  |  |
| 2 | `LevelNum` | Level No. | Int | 11 | - |  |  |
| 3 | `LetterFrmt` | Letter Format | nVarChar | 8 | - |  |  |
| 4 | `EffctAftr` | Effective after | nVarChar | 3 | - |  |  |
| 5 | `LetterFee` | Fee per Letter | Num | 19.6 | - |  |  |
| 6 | `FeeCurr` | Fee Currency | nVarChar | 3 | - |  |  |
| 7 | `MinBalance` | Mininum Balance | Num | 19.6 | - |  |  |
| 8 | `MinBlnCurr` | Min Balance Currency | nVarChar | 3 | - |  |  |
| 9 | `CalcIntrst` | Calc. Interest | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TermCode, LevelNum |
