# OSSG - Service App Setting groups

- **Tabla:** OSSG
- **Descripción:** Service App Setting groups
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSSG.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Code | Int | 11 | - |  |  |
| 2 | `Name` | Name | nVarChar | 100 | - |  |  |
| 3 | `CustGroup` | Customized Group | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 4 | `EnEditTime` | Enable Edit Time | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 5 | `EnReject` | Enable Reject | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `EnResign` | Enable Resign | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 7 | `EnFollowup` | Enable Follow-up | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `EnSign` | Enable Signature | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 9 | `EnStarRat` | Enable Star Rating | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 10 | `EnActDura` | Enable Actual Duration | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 11 | `AdBoardId` | Advanced Dashboard ID | Int | 11 | [OXAP](OXAP.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code |
