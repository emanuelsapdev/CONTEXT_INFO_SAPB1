# DAR2 - Data Archive - Transaction Log

- **Tabla:** DAR2
- **Descripción:** Data Archive - Transaction Log
- **Cantidad de campos:** 20
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/DAR2.html

## Campos (20)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ArcEntry` | Data Archive Entry | Int | 11 | - |  |  |
| 2 | `Line_ID` | Row Number | Int | 11 | - | 0 |  |
| 3 | `Approve` | Approve | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 4 | `DocType` | Document Type | Int | 11 | - |  |  |
| 5 | `DocNum` | Document Number | Int | 11 | - |  |  |
| 6 | `DocAbs` | Document Abs Entry | Int | 11 | - |  |  |
| 7 | `CardCode` | Customer/Vendor Code | nVarChar | 15 | - |  |  |
| 8 | `RefDate` | Posting Date | Date | 8 | - |  |  |
| 9 | `DueDate` | Due Date | Date | 8 | - |  |  |
| 10 | `TaxDate` | Document Date | Date | 8 | - |  |  |
| 11 | `Total` | Total | Num | 19.6 | - |  |  |
| 12 | `Action` | Action | VarChar | 1 | - | T | `R` = Remove<br>`L` = Locked<br>`T` = Temporary |
| 13 | `Remarks` | Remarks | nVarChar | 50 | - |  |  |
| 14 | `KeySeg1` | Key Segment 1 | nVarChar | 15 | - |  |  |
| 15 | `KeySeg2` | Key Segment 2 | nVarChar | 15 | - |  |  |
| 16 | `KeySeg3` | Key Segment 3 | nVarChar | 15 | - |  |  |
| 17 | `KeySeg4` | Key Segment 4 | nVarChar | 15 | - |  |  |
| 18 | `KeySeg5` | Key Segment 5 | nVarChar | 15 | - |  |  |
| 19 | `KeySeg6` | Key Segment 6 | nVarChar | 15 | - |  |  |
| 20 | `ClusterId` | Cluster ID | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ArcEntry, Line_ID |
