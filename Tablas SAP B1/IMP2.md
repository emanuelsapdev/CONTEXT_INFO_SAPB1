# IMP2 - Import Row Details and Status

- **Tabla:** IMP2
- **Descripción:** Import Row Details and Status
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/IMP2.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `SessionId` | Session ID | Int | 11 | - |  |  |
| 2 | `TableName` | Table Name | nVarChar | 100 | - |  |  |
| 3 | `RowNumber` | RowNumber | Int | 6 | - |  |  |
| 4 | `ImportMtd` | Import Method | nVarChar | 2 | - | AO | `AU` = Add new records and update existing records<br>`AO` = Add new records without updating existing records<br>`UO` = Update existing records without adding new records |
| 5 | `Validation` | Validation Result | VarChar | 1 | - |  | `N` = Invalid<br>`Y` = Ready<br>`R` = Ready* |
| 6 | `Simulation` | Simulation Result | VarChar | 1 | - |  | `N` = Not Simulated<br>`V` = Simulation Successful<br>`E` = Error in Simulation |
| 7 | `ImptStatus` | Import Status | nVarChar | 2 | - |  | `A` = Added<br>`U` = Updated<br>`F` = Failed<br>`S` = Skipped |
| 8 | `ImpMsg` | Import Message for Skipped or Failed Records | nVarChar | 200 | - |  |  |
| 9 | `ErrMsg` | Row-level simulation or special use case error message | nVarChar | 200 | - |  |  |
| 10 | `ImportLog` | Import Log | nVarChar | 50 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | SessionId, RowNumber |
