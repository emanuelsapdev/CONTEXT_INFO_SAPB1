# OWFI - Workflow - Instances

- **Tabla:** OWFI
- **Descripción:** Workflow - Instances
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OWFI.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WFInstID` | WF Instance ID | Identity | 11 | - |  |  |
| 2 | `ExecID` | WF Instance on Engine | Int | 11 | - |  |  |
| 3 | `TemplateID` | WF Template ID | Int | 11 | - |  |  |
| 4 | `Creator` | Creator | nVarChar | 25 | - |  |  |
| 5 | `Status` | Status | nVarChar | 8 | - |  | `S` = Setup<br>`F` = Completed<br>`G` = In Progress<br>`C` = Cancelling<br>`Q` = Canceled<br>`E` = Error |
| 6 | `StartDate` | Start Date | Date | 8 | - |  |  |
| 7 | `StartTime` | Start Time | Int | 6 | - |  |  |
| 8 | `EndTime` | End Time | Int | 6 | - |  |  |
| 9 | `EndDate` | End Date | Date | 8 | - |  |  |
| 10 | `IsAutoStar` | Is auto start instance | Int | 6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WFInstID |
