# PRS1 - Detail Lines of Print Sequence Definition

- **Tabla:** PRS1
- **Descripción:** Detail Lines of Print Sequence Definition
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/PRS1.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `SeqID` | Internal Number | Int | 11 | - |  |  |
| 2 | `LineNum` | Row Number | Int | 6 | - |  |  |
| 3 | `ObjectID` | Document Object ID | Int | 11 | - |  |  |
| 4 | `LaytCode` | Report Code | nVarChar | 8 | - |  |  |
| 5 | `NumCopy` | Number of Copies | Int | 6 | - |  |  |
| 6 | `UsrQuery` | User Query to Customize | Int | 11 | - |  |  |
| 7 | `SubDocType` | Document Subtype | Int | 6 | - |  |  |
| 8 | `Printer` | Printer | nVarChar | 100 | - |  |  |
| 9 | `Prtr1st` | Printer for First Page | nVarChar | 100 | - |  |  |
| 10 | `Use1stPrtr` | Use 1st Page Printer | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | SeqID, LineNum |
