# OSCS - Service Call Statuses

- **Tabla:** OSCS
- **Descripción:** Service Call Statuses
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSCS.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `statusID` | Status ID | Int | 6 | - |  |  |
| 2 | `Name` | Name | nVarChar | 20 | - |  |  |
| 3 | `Descriptio` | Description | Text | 16 | - |  |  |
| 4 | `Locked` | Locked | VarChar | 1 | - |  |  |
| 5 | `Active` | Active | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | statusID |
| NAME | No | Name |
