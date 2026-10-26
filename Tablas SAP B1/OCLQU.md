# OCLQU - User Settings for "Ask AI" App in Web Client

- **Tabla:** OCLQU
- **Descripción:** User Settings for "Ask AI" App in Web Client
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCLQU.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Id` | ID | Int | 11 | - |  |  |
| 2 | `QuestionId` | Question ID | Int | 11 | [OCLQ](OCLQ.md) |  |  |
| 3 | `UserId` | User ID | Int | 11 | - |  |  |
| 4 | `IsActive` | Is Active | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 5 | `DataVers` | Data Version | Int | 11 | - | 1 |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Id |
| PARENT_USR | Yes | QuestionId, UserId |
