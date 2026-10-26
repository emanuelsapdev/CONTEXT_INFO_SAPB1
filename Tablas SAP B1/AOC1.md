# AOC1 - Distribution Rule - Rows

- **Tabla:** AOC1
- **Descripción:** Distribution Rule - Rows
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AOC1.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `OcrCode` | Factor Code | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 2 | `PrcCode` | Cost Center Code | nVarChar | 8 | [OPRC](OPRC.md) |  |  |
| 3 | `PrcAmount` | Total in Cost Center | Num | 19.6 | - |  |  |
| 4 | `OcrTotal` | Total Factor | Num | 19.6 | - |  |  |
| 5 | `Direct` | Direct | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 7 | `ValidFrom` | Effective from | Date | 8 | - |  |  |
| 8 | `ValidTo` | Effective to | Date | 8 | - |  |  |
| 9 | `logInstanc` | Log Instance | Int | 11 | - |  |  |
| 10 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 11 | `updateDate` | Date of Update | Date | 8 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | OcrCode, PrcCode, ValidFrom, logInstanc |
| PROF_ID | No | PrcCode |
