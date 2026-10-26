# OATB - Administration

- **Tabla:** OATB
- **Descripción:** Administration
- **Cantidad de campos:** 2
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OATB.html

## Campos (2)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `IsAbandon` | Is This File Type Abandoned | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 2 | `FileType` | File Type | nVarChar | 20 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | FileType |
