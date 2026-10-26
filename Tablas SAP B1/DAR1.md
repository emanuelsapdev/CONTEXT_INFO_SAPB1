# DAR1 - Data Archive - Transaction Log

- **Tabla:** DAR1
- **Descripción:** Data Archive - Transaction Log
- **Cantidad de campos:** 25
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/DAR1.html

## Campos (25)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ArcEntry` | Data Archive Entry | Int | 11 | - |  |  |
| 2 | `Line_ID` | Row Number | Int | 11 | - |  |  |
| 3 | `DocType` | Document Type | nVarChar | 20 | - |  |  |
| 4 | `DocNum` | Document Number | Int | 11 | - |  |  |
| 5 | `DocAbs` | Document Internal ID | Int | 11 | - |  |  |
| 6 | `Total` | Total | Num | 19.6 | - |  |  |
| 7 | `RefDate` | Posting Date | Date | 8 | - |  |  |
| 8 | `ClusterId` | Cluster ID | Int | 11 | - |  |  |
| 9 | `Remarks` | Remarks | nVarChar | 100 | - |  |  |
| 10 | `KeySeg1` | Key Segment 1 | nVarChar | 15 | - |  |  |
| 11 | `KeySeg2` | Key Segment 2 | nVarChar | 15 | - |  |  |
| 12 | `KeySeg3` | Key Segment 3 | nVarChar | 15 | - |  |  |
| 13 | `KeySeg4` | Key Segment 4 | nVarChar | 15 | - |  |  |
| 14 | `KeySeg5` | Key Segment 5 | nVarChar | 15 | - |  |  |
| 15 | `KeySeg6` | Key Segment 6 | nVarChar | 15 | - |  |  |
| 16 | `KeySeg7` | Key Segment 7 | nVarChar | 20 | - |  |  |
| 17 | `KeySeg8` | Key Segment 8 | nVarChar | 15 | - |  |  |
| 18 | `KeySeg9` | Key Segment 9 | nVarChar | 15 | - |  |  |
| 19 | `KeySeg10` | Key Segment 10 | nVarChar | 15 | - |  |  |
| 20 | `Series` | Series | Int | 11 | - |  |  |
| 21 | `DocSubType` | Document Sub-Type | nVarChar | 2 | - | -- |  |
| 22 | `PIndicator` | Period Indicator | nVarChar | 10 | - | ' ' |  |
| 23 | `Instance` | Instance | Int | 6 | - | 0 |  |
| 24 | `Segment` | Segment | Int | 6 | - | 0 |  |
| 25 | `CardCode` | Card Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ArcEntry, Line_ID |
| ABS_TYPE | No | DocAbs, DocType |
