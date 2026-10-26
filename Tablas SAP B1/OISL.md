# OISL - Simulation Log File

- **Tabla:** OISL
- **Descripción:** Simulation Log File
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OISL.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `LogEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `TaskType` | Type of Task | nVarChar | 20 | - |  |  |
| 3 | `RunID` | Simulation Run | Int | 11 | - |  |  |
| 4 | `Version` | B1 Main Release Version | Int | 11 | - |  |  |
| 5 | `PatchLevel` | B1 Patch Level Version | nVarChar | 50 | - |  |  |
| 6 | `LastMsgID` | Last OILM Message ID | Int | 11 | - |  |  |
| 7 | `FinishDate` | Finish Date | Date | 8 | - |  |  |
| 8 | `FinishTime` | Finish Time | Int | 6 | - |  |  |
| 9 | `UserCode` | User Code | nVarChar | 25 | - |  |  |
| 10 | `Status` | Status | VarChar | 1 | - |  | `R` = In Progress<br>`F` = Failed<br>`S` = Successful |
| 11 | `InitMap` | Initialize MAP Items | VarChar | 1 | - |  |  |
| 12 | `InitStd` | Initialize STD Items | VarChar | 1 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | LogEntry |
