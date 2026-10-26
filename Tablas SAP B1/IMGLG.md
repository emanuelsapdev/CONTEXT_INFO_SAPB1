# IMGLG - Group Message Log

- **Tabla:** IMGLG
- **Descripción:** Group Message Log
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/IMGLG.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Id` | Internal Number | Identity | 11 | - |  |  |
| 2 | `From` | Message Sender | nVarChar | 25 | - |  |  |
| 3 | `GrpId` | Group ID | Int | 11 | - |  |  |
| 4 | `Msg` | Message Content | Text | 16 | - |  |  |
| 5 | `Time` | Time | Date | 8 | - |  |  |
| 6 | `Nty` | Is Notification | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Id |
