# DAR4 - Data Archive - Candidate

- **Tabla:** DAR4
- **Descripción:** Data Archive - Candidate
- **Cantidad de campos:** 20
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/DAR4.html

## Campos (20)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ArcEntry` | Data Archive Entry | Int | 11 | - |  |  |
| 2 | `Series` | Series | Int | 11 | - |  |  |
| 3 | `Line_ID` | Row Number | Int | 11 | - |  |  |
| 4 | `DocType` | Document Type | nVarChar | 20 | - |  |  |
| 5 | `DocNum` | Document Number | Int | 11 | - |  |  |
| 6 | `DocAbs` | Document Internal ID | Int | 11 | - |  |  |
| 7 | `Total` | Total | Num | 19.6 | - |  |  |
| 8 | `RefDate` | Posting Date | Date | 8 | - |  |  |
| 9 | `Type` | Type | VarChar | 1 | - | R | `R` = Recommendation<br>`M` = Marked |
| 10 | `Remarks` | Remarks | nVarChar | 100 | - |  |  |
| 11 | `KeySeg1` | Key Segment 1 | nVarChar | 15 | - |  |  |
| 12 | `KeySeg2` | Key Segment 2 | nVarChar | 15 | - |  |  |
| 13 | `KeySeg3` | Key Segment 3 | nVarChar | 15 | - |  |  |
| 14 | `KeySeg4` | Key Segment 4 | nVarChar | 15 | - |  |  |
| 15 | `KeySeg5` | Key Segment 5 | nVarChar | 15 | - |  |  |
| 16 | `KeySeg6` | Key Segment 6 | nVarChar | 15 | - |  |  |
| 17 | `KeySeg7` | Key Segment 7 | nVarChar | 20 | - |  |  |
| 18 | `KeySeg8` | Key Segment 8 | nVarChar | 15 | - |  |  |
| 19 | `KeySeg9` | Key Segment 9 | nVarChar | 15 | - |  |  |
| 20 | `KeySeg10` | Key Segment 10 | nVarChar | 15 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ArcEntry, Line_ID |
| ABS_TYPE | No | DocAbs, DocType |
