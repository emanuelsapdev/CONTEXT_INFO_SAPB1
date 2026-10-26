# DGP6 - Document Generation Parameters

- **Tabla:** DGP6
- **Descripción:** Document Generation Parameters
- **Cantidad de campos:** 24
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/DGP6.html

## Campos (24)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number Wizard ID | Int | 11 | - |  |  |
| 2 | `BaseEntry` | Base Entry | Int | 11 | - |  |  |
| 3 | `RunUser` | Run User ID | Int | 6 | - |  |  |
| 4 | `RunDate` | Job Running Date | Date | 8 | - |  |  |
| 5 | `RunTime` | Job Running Time | Int | 6 | - |  |  |
| 6 | `CardCode` | Customer Code | nVarChar | 15 | - |  |  |
| 7 | `QUTDocList` | Sales Quotation Document List | Text | 16 | - |  |  |
| 8 | `RDRDocList` | Sales Order Document List | Text | 16 | - |  |  |
| 9 | `INVDocList` | A/R Reserve Invoice Document List | Text | 16 | - |  |  |
| 10 | `DLNDocList` | Delivery Document List | Text | 16 | - |  |  |
| 11 | `ObjType` | Target Object Type | nVarChar | 20 | - | 13 |  |
| 12 | `DocDate` | Posting Date | Date | 8 | - |  |  |
| 13 | `DocDueDate` | Due Date | Date | 8 | - |  |  |
| 14 | `TaxDate` | Tax Date | Date | 8 | - |  |  |
| 15 | `CardName` | Customer Name | nVarChar | 200 | - |  |  |
| 16 | `NumAtCard` | BP Reference No. | nVarChar | 200 | - |  |  |
| 17 | `Address` | Bill To | nVarChar | 254 | - |  |  |
| 18 | `Address2` | Ship To | nVarChar | 254 | - |  |  |
| 19 | `Comments` | Remarks | nVarChar | 254 | - |  |  |
| 20 | `JrnlMemo` | Journal Remarks | nVarChar | 254 | - |  |  |
| 21 | `Project` | Project Code | nVarChar | 20 | - |  |  |
| 22 | `OwnerCode` | Document Owner | Int | 11 | - |  |  |
| 23 | `SlpCode` | Sales Employee | Int | 11 | - | -1 |  |
| 24 | `TrnspCode` | Shipping Type | Int | 6 | - | -1 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, BaseEntry, RunUser, RunDate, RunTime, CardCode |
