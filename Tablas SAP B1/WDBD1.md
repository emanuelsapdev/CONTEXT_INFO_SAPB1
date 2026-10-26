# WDBD1 - Dashboard Cards

- **Tabla:** WDBD1
- **Descripción:** Dashboard Cards
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WDBD1.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ParentId` | Parent Id | nVarChar | 40 | - |  |  |
| 2 | `Guid` | Guid | nVarChar | 40 | - |  |  |
| 3 | `UserId` | User Id | Int | 11 | - |  |  |
| 4 | `Content` | Content | Text | 16 | - |  |  |
| 5 | `Sys` | Sys | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 6 | `Version` | Version | nVarChar | 40 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ParentId, Guid |
