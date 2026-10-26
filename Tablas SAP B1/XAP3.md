# XAP3 - XAP Filter

- **Tabla:** XAP3
- **Descripción:** XAP Filter
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/XAP3.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Key of XAPP filter | Int | 11 | - |  |  |
| 2 | `XAPEntry` | Foreign key of XAPP | Int | 11 | - |  |  |
| 3 | `Name` | Name of filter | nVarChar | 250 | - |  |  |
| 4 | `Type` | Type of filter | nVarChar | 250 | - |  |  |
| 5 | `Method` | Filter method | nVarChar | 250 | - |  |  |
| 6 | `MultiValue` | Allow multiple value | VarChar | 1 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
