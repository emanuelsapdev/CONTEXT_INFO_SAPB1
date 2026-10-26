# ORTY - Web Client Report Types

- **Tabla:** ORTY
- **Descripción:** Web Client Report Types
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ORTY.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Report Type Code | nVarChar | 32 | - |  |  |
| 2 | `Name` | Report Type Name | nVarChar | 250 | - |  |  |
| 3 | `MenuId` | Report Menu Id | nVarChar | 250 | - |  |  |
| 4 | `IsSystem` | Is System | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code |
