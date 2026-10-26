# UWOR4 - Production Order - Route Stages

- **Tabla:** UWOR4
- **Descripción:** Production Order - Route Stages
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/UWOR4.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal Number | Int | 11 | [OWOR](OWOR.md) |  |  |
| 2 | `StageId` | Stage ID | Int | 11 | - |  |  |
| 3 | `SeqNum` | Sequence Number | Int | 11 | - |  |  |
| 4 | `StgEntry` | Stage Entry | Int | 11 | [ORST](ORST.md) |  |  |
| 5 | `Name` | Stage Name | nVarChar | 100 | - |  |  |
| 6 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 7 | `StartDate` | Start Date | Date | 8 | - |  |  |
| 8 | `EndDate` | End Date | Date | 8 | - |  |  |
| 9 | `Status` | Stage Status | VarChar | 1 | - | P | `P` = Planned<br>`I` = In Progress<br>`C` = Complete |
| 10 | `RtCalcProp` | Routing Calculation Proportion | Num | 19.6 | - | 100 |  |
| 11 | `ReqDays` | Required Days | Num | 19.6 | - | 0 |  |
| 12 | `WaitDays` | Waiting Days | Num | 19.6 | - | 0 |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, StageId |
| SEQUENCE | Yes | DocEntry, SeqNum |
