# LIVI1 - IVI Log Array File

- **Tabla:** LIVI1
- **Descripción:** IVI Log Array File
- **Cantidad de campos:** 14
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/LIVI1.html

## Campos (14)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `LogEntry` | Internal Number | Int | 11 | [LIVI](LIVI.md) |  |  |
| 2 | `CalcNum` | Partial Sequence Number | Int | 11 | - |  |  |
| 3 | `CreateDate` | Create Date | Date | 8 | - |  |  |
| 4 | `UserToDate` | User To Date | Date | 8 | - |  |  |
| 5 | `ActuToDate` | Actual To Date | Date | 8 | - |  |  |
| 6 | `LastMsgID` | Last Calculated OILM Message | Int | 11 | - |  |  |
| 7 | `Result` | Result of Calculation | VarChar | 1 | - | F | `F` = Failure<br>`S` = Success<br>`A` = Archived |
| 8 | `ResultStr` | Result String of Calculation | nVarChar | 254 | - |  |  |
| 9 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 10 | `IgnFail` | Ignore Previous Failure | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 11 | `ReorderFrm` | Reorder 8.8 Messages: From Date | Date | 8 | - |  |  |
| 12 | `ReorderTo` | Reorder 8.8 Messages: To Date | Date | 8 | - |  |  |
| 13 | `StopDate` | Stop Date | Date | 8 | - |  |  |
| 14 | `StopTime` | Stop Time | Int | 6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | LogEntry, CalcNum |
