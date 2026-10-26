# AWTS - Workflow Engine Task Table

- **Tabla:** AWTS
- **Descripción:** Workflow Engine Task Table
- **Cantidad de campos:** 17
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AWTS.html

## Campos (17)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Id` | ID | Int | 11 | - |  |  |
| 2 | `Owner` | Owner | nVarChar | 254 | - |  |  |
| 3 | `OutputPar` | Output Parameter | Text | 16 | - |  |  |
| 4 | `EndTime` | End Time | nVarChar | 50 | - |  |  |
| 5 | `StartTime` | Start Time | nVarChar | 50 | - |  |  |
| 6 | `ProcDefId` | Process Definition ID | Int | 11 | - |  |  |
| 7 | `Name` | Name | nVarChar | 254 | - |  |  |
| 8 | `ExeId` | Execution ID | Int | 11 | - |  |  |
| 9 | `ProcInsId` | Process Instance ID | Int | 11 | - |  |  |
| 10 | `Desc` | Description | nVarChar | 254 | - |  |  |
| 11 | `InputPar` | Input Parameter | Text | 16 | - |  |  |
| 12 | `DelReason` | Delete Reason | nVarChar | 254 | - |  |  |
| 13 | `Assignee` | Assignee | nVarChar | 254 | - |  |  |
| 14 | `LogInst` | Log Instance | Int | 11 | - |  |  |
| 15 | `LastUpdate` | Last Update Date | nVarChar | 50 | - |  |  |
| 16 | `Key` | Task ID in XML | nVarChar | 254 | - |  |  |
| 17 | `B1Task` | B1 Task ID | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Id, LogInst |
