# ODUN - Dunning Letters

- **Tabla:** ODUN
- **Descripción:** Dunning Letters
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ODUN.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 2 | `LetrFormat` | Letter Format | nVarChar | 8 | - |  |  |
| 3 | `EffctAftr` | Effective After (Days) | nVarChar | 3 | - |  |  |
| 4 | `LetterFee` | Fee Per Letter | Num | 19.6 | - |  |  |
| 5 | `FeeCurr` | Fee Currency | nVarChar | 3 | - |  |  |
| 6 | `MinBalance` | Minimum Balance | Num | 19.6 | - |  |  |
| 7 | `MinBlnCurr` | Minimum Balance Currency | nVarChar | 3 | - |  |  |
| 8 | `CalcIntert` | Interest | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | LineNum |
