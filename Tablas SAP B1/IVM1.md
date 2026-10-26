# IVM1 - Invoice Mapping Object Details

- **Tabla:** IVM1
- **Descripción:** Invoice Mapping Object Details
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/IVM1.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [OIVM](OIVM.md) |  |  |
| 2 | `LineNum` | Line Number | Int | 11 | - |  |  |
| 3 | `DocType` | Document Type | nVarChar | 20 | - |  |  |
| 4 | `DocEntry` | Document Entry | Int | 11 | - |  |  |
| 5 | `GtsStatus` | GTS Status | VarChar | 1 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineNum |
