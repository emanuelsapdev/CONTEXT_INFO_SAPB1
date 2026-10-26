# OCLA - Activity Status

- **Tabla:** OCLA
- **Descripción:** Activity Status
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCLA.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `statusID` | Status ID | Int | 11 | - |  |  |
| 2 | `name` | Status Name | nVarChar | 30 | - |  |  |
| 3 | `descriptio` | Status Description | nVarChar | 254 | - |  |  |
| 4 | `Locked` | Locked | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | statusID |
