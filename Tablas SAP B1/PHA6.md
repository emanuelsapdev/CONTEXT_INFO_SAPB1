# PHA6 - Project Management - Stages - Activities

- **Tabla:** PHA6
- **Descripción:** Project Management - Stages - Activities
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/PHA6.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | [PHA1](PHA1.md) |  |  |
| 2 | `LineID` | Row No. | Int | 11 | - |  |  |
| 3 | `StageID` | Stage ID | Int | 11 | - |  |  |
| 4 | `ACTIVITYID` | Activity Number | Int | 11 | [OCLG](OCLG.md) |  |  |
| 5 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 6 | `Charged` | Charged | Num | 19.6 | - |  |  |
| 7 | `Chargeable` | Chargeable [Yes/No] | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 8 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineID |
