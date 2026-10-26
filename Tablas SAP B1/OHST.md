# OHST - Employee Status

- **Tabla:** OHST
- **Descripción:** Employee Status
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OHST.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `statusID` | Status ID | Int | 11 | - |  |  |
| 2 | `name` | Name | nVarChar | 20 | - |  |  |
| 3 | `descriptio` | Description | Text | 16 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | statusID |
| NAME_KEY | Yes | name |
