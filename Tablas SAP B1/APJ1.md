# APJ1 - Project Plan Steps

- **Tabla:** APJ1
- **Descripción:** Project Plan Steps
- **Cantidad de campos:** 20
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/APJ1.html

## Campos (20)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `StepCode` | Step Code | Int | 11 | - |  |  |
| 3 | `Father` | Father Step Code | Int | 11 | - |  |  |
| 4 | `VisOrder` | Visual Order | Int | 11 | - |  |  |
| 5 | `Level` | Node Level | Int | 11 | - |  |  |
| 6 | `StepName` | Step Name | nVarChar | 254 | - |  |  |
| 7 | `StepInfo` | Step Info | nVarChar | 254 | - |  |  |
| 8 | `StepNotes` | Step Notes | nVarChar | 254 | - |  |  |
| 9 | `StepLink` | Step Link to Menu ID | nVarChar | 32 | - |  |  |
| 10 | `StartDate` | Start Date | Date | 8 | - |  |  |
| 11 | `EndDate` | End Date | Date | 8 | - |  |  |
| 12 | `IsComplete` | Is Complete | VarChar | 1 | - |  |  |
| 13 | `LogInstanc` | Log Instance | Int | 11 | - |  |  |
| 14 | `Owner` | Owner | nVarChar | 254 | [OUSR](OUSR.md) |  |  |
| 15 | `Status` | Status | Int | 11 | - | 0 |  |
| 16 | `Duration` | Duration | Num | 19.6 | - |  |  |
| 17 | `PlanTime` | Planned Time | Num | 19.6 | - |  |  |
| 18 | `AtcEntry` | Attachment Entry | Int | 11 | [OATC](OATC.md) |  |  |
| 19 | `TotalPTime` | Total Planned Time | Num | 19.6 | - |  |  |
| 20 | `QueryID` | Step Link Query ID | Int | 11 | [OUQR](OUQR.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, StepCode, LogInstanc |
