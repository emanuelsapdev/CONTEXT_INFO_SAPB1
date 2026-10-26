# TRS1 - Tax Report Saving Object - Approved Documents

- **Tabla:** TRS1
- **Descripción:** Tax Report Saving Object - Approved Documents
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TRS1.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [OTRS](OTRS.md) |  |  |
| 2 | `ObjType` | Object Type | nVarChar | 20 | - |  |  |
| 3 | `LineID` | Internal Row Number | Int | 11 | - |  |  |
| 4 | `ApDocType` | Approved Document Type | nVarChar | 20 | - |  |  |
| 5 | `ApDocEntry` | Approved Document Key | Int | 11 | - |  |  |
| 6 | `ApDocOrdNo` | Appr. Doc. Ordinal Number | Int | 11 | - | -1 |  |
| 7 | `ApDocAdRef` | Appr. Doc. Additional Reference | Int | 11 | - | -1 |  |
| 8 | `MeansType` | Payment Means Type | Int | 11 | - | -1 |  |
| 9 | `PayLineID` | Payment Means Line ID | Int | 11 | - | -1 |  |
| 10 | `PayDocType` | Payment Document Type | Int | 11 | - | -1 |  |
| 11 | `PayDocEntr` | Payment Document Entry | Int | 11 | - | -1 |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineID |
| SECONDARY | Yes | AbsEntry, ApDocType, ApDocEntry, ApDocOrdNo, MeansType, PayLineID, PayDocType, PayDocEntr |
