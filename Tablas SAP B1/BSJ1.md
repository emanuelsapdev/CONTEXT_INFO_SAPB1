# BSJ1 - Backend Scheduling Sub Tasks

- **Tabla:** BSJ1
- **Descripción:** Backend Scheduling Sub Tasks
- **Cantidad de campos:** 14
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/BSJ1.html

## Campos (14)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ID` | Job ID | Int | 11 | [OBSJ](OBSJ.md) |  |  |
| 2 | `TaskID` | Sub Task ID | Int | 11 | - |  |  |
| 3 | `Type` | Task Type | nVarChar | 50 | - |  |  |
| 4 | `Params` | Parameters | Text | 16 | - |  |  |
| 5 | `RunAs` | Run As User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 6 | `Status` | Status | VarChar | 1 | - | S | `S` = Scheduled<br>`R` = Running<br>`E` = Error<br>`F` = Finished<br>`P` = Pending<br>`C` = Creating |
| 7 | `PostTask` | Post-Task | Int | 11 | - |  |  |
| 8 | `PreTask` | Pre-Task | Int | 11 | - |  |  |
| 9 | `LastDate` | Last Running Date | Date | 8 | - |  |  |
| 10 | `LastTime` | Last Running Time | Int | 6 | - |  |  |
| 11 | `Duration` | Duration | Num | 19.6 | - |  |  |
| 12 | `Retry` | Retry Times | Int | 11 | - | 0 |  |
| 13 | `TimeOut` | Time out | Int | 11 | - | 20 |  |
| 14 | `Message` | Status Message | nVarChar | 200 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ID, TaskID |
