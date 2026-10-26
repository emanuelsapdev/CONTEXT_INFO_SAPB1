# ORTL - Resource Transaction Log

- **Tabla:** ORTL
- **Descripción:** Resource Transaction Log
- **Cantidad de campos:** 24
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ORTL.html

## Campos (24)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `LogEntry` | Log Entry ID | Int | 11 | - |  |  |
| 2 | `ResCode` | Resource Code | nVarChar | 50 | [ORSC](ORSC.md) |  |  |
| 3 | `DocType` | Transact. Type | Int | 11 | - |  |  |
| 4 | `DocEntry` | Document Internal ID | Int | 11 | - |  |  |
| 5 | `DocLine` | Doc. Row Number | Int | 11 | - |  |  |
| 6 | `BaseType` | Base Document Type | Int | 11 | - |  |  |
| 7 | `BaseEntry` | Base Document Internal ID | Int | 11 | - |  |  |
| 8 | `BaseLine` | Base Document Row Number | Int | 11 | - |  |  |
| 9 | `ActionType` | Action Type | Int | 11 | - | 0 | `0` = RESOURCE_TRANSACTION_UNKNOWN<br>`1` = RESOURCE_TRANSACTION_IN<br>`2` = RESOURCE_TRANSACTION_OUT |
| 10 | `LocType` | Location Type | Int | 6 | - |  |  |
| 11 | `LocCode` | Location Code | nVarChar | 8 | - |  |  |
| 12 | `VersionNum` | Version Number | nVarChar | 13 | - |  |  |
| 13 | `PostDate` | Posting Date | Date | 8 | - |  |  |
| 14 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 15 | `CreateTime` | Creation Time | Int | 6 | - |  |  |
| 16 | `DocQty` | Doc. Quantity | Num | 19.6 | - |  |  |
| 17 | `Price` | Price | Num | 19.6 | - |  |  |
| 18 | `LineTotal` | Row Total | Num | 19.6 | - |  |  |
| 19 | `OpenQty` | Open Quantity | Num | 19.6 | - |  |  |
| 20 | `DocNum` | Document Number | nVarChar | 11 | - |  |  |
| 21 | `BaseDocNum` | Base Document Number | nVarChar | 11 | - |  |  |
| 22 | `StgSeqNum` | Stage Sequence Number | Int | 11 | - |  |  |
| 23 | `StgEntry` | Stage Entry | Int | 11 | - |  |  |
| 24 | `StgDesc` | Stage Description | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | LogEntry |
