# MSN5 - MRP-Specific Document

- **Tabla:** MSN5
- **Descripción:** MRP-Specific Document
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MSN5.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `DocType` | Document Type | nVarChar | 20 | - |  |  |
| 3 | `DocEntry` | Document Entry | Int | 11 | - |  |  |
| 4 | `Selected` | Selected | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 5 | `DocSubType` | Document Sub-Type | nVarChar | 2 | - | -- |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, DocType, DocEntry, DocSubType |
