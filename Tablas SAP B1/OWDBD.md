# OWDBD - Dashboard Overview

- **Tabla:** OWDBD
- **Descripción:** Dashboard Overview
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OWDBD.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Guid` | Guid | nVarChar | 40 | - |  |  |
| 2 | `UserId` | User Id | Int | 11 | - |  |  |
| 3 | `Content` | Content | Text | 16 | - |  |  |
| 4 | `Sys` | Sys | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Guid |
