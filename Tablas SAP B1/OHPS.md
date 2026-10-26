# OHPS - Employee Position

- **Tabla:** OHPS
- **Descripción:** Employee Position
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OHPS.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `posID` | Item ID | Int | 11 | - |  |  |
| 2 | `name` | Position Name | nVarChar | 20 | - |  |  |
| 3 | `descriptio` | Description | Text | 16 | - |  |  |
| 4 | `LocFields` | Activate Localization Fields | VarChar | 1 | - | N | `Y`<br>`N` |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | posID |
| NAME | Yes | name |
