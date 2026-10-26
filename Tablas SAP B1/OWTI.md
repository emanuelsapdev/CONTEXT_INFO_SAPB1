# OWTI - Workflow Timer Definition

- **Tabla:** OWTI
- **Descripción:** Workflow Timer Definition
- **Cantidad de campos:** 15
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OWTI.html

## Campos (15)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Id` | ID | Identity | 11 | - |  |  |
| 2 | `Name` | Name | nVarChar | 50 | - |  |  |
| 3 | `TemplateId` | Workflow Template ID | Int | 11 | - |  |  |
| 4 | `StartDate` | Start Date | Date | 8 | - |  |  |
| 5 | `StartTime` | Start Time | Int | 11 | - |  |  |
| 6 | `RepeatCnt` | Repeat Event Count | Int | 11 | - |  |  |
| 7 | `Duration` | Duration | nVarChar | 200 | - |  |  |
| 8 | `LastUpdate` | Last Update Date and Time | nVarChar | 50 | - |  |  |
| 9 | `UnScheStDt` | Start Date of Next Schedule | Date | 8 | - |  |  |
| 10 | `UnScheStTi` | Start Time of Next Schedule | Int | 11 | - |  |  |
| 11 | `UnScheReCt` | Unschedule Repeat Count | Int | 11 | - |  |  |
| 12 | `IsComplete` | Is This Timer Completed | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 13 | `JobHanType` | Job Handler Type | nVarChar | 50 | - |  |  |
| 14 | `JobHanConf` | Job Handler Configuration | Text | 16 | - |  |  |
| 15 | `IsActive` | Is This an Active Timer | VarChar | 1 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Id |
