# OUPT - User Autorization Tree

- **Tabla:** OUPT
- **Descripción:** User Autorization Tree
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OUPT.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Authorization ID | nVarChar | 20 | - |  |  |
| 2 | `Name` | Name | nVarChar | 64 | - |  |  |
| 3 | `Options` | Options | Int | 6 | - | 0 | `0` = Full/Read/None<br>`1` = Full/None |
| 4 | `FathId` | Parent ID | nVarChar | 20 | [OUPT](OUPT.md) |  |  |
| 5 | `VisOrder` | Display Order | Int | 6 | - |  |  |
| 6 | `Levels` | Levels | Int | 6 | - | 1 |  |
| 7 | `IsItem` | IS Item | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `Action` | Action | Int | 6 | - |  |  |
| 9 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId |
