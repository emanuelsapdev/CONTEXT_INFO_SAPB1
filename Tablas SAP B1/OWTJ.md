# OWTJ - Workflow Timer Job

- **Tabla:** OWTJ
- **Descripción:** Workflow Timer Job
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OWTJ.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Id` | ID | Identity | 11 | - |  |  |
| 2 | `IsASync` | Is Asychronized | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 3 | `Status` | Status | nVarChar | 10 | - |  |  |
| 4 | `StartDate` | Start Date | Date | 8 | - |  |  |
| 5 | `StartTime` | Start Time | Int | 11 | - |  |  |
| 6 | `TimerEtyId` | Timer Entity ID | Int | 11 | - |  |  |
| 7 | `JobHanConf` | Job Handler Configuration | Text | 16 | - |  |  |
| 8 | `JobHanType` | Job Handler Type | nVarChar | 50 | - |  |  |
| 9 | `LastUpdate` | Last Update Date and Time | nVarChar | 50 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Id |
