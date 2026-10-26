# OHED - Education Types

- **Tabla:** OHED
- **Descripción:** Education Types
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OHED.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `edType` | Education Type | Int | 11 | - |  |  |
| 2 | `name` | Name | nVarChar | 20 | - |  |  |
| 3 | `descriptio` | Description | Text | 16 | - |  |  |
| 4 | `Locked` | Locked | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | edType |
| NAME_KEY | Yes | name |
