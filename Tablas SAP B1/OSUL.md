# OSUL - Support User Login Record

- **Tabla:** OSUL
- **Descripción:** Support User Login Record
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSUL.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ID` | Main ID | Int | 11 | - |  |  |
| 2 | `RealName` | Real Name | nVarChar | 100 | - |  |  |
| 3 | `LogReason` | Login Reason | nVarChar | 100 | - |  | `A` = Transaction Issue Analysis<br>`B` = Setup Issue Analysis<br>`C` = Data Issue Analysis<br>`D` = Add-on Issue Analysis<br>`E` = Customer Usage Assistance<br>`F` = System Maintenance<br>`G` = Consulting<br>`I` = Add-on Access<br>`J` = Root Cause Analysis<br>`K` = Consulting / Support<br>`H` = Other |
| 4 | `LogDetail` | Login Detail Information | Text | 16 | - |  |  |
| 5 | `Mac` | MAC Address | nVarChar | 100 | - |  |  |
| 6 | `Machine` | Machine Name | nVarChar | 100 | - |  |  |
| 7 | `StartDate` | Start Date | Date | 8 | - |  |  |
| 8 | `StartTime` | Start Time | Int | 11 | - |  |  |
| 9 | `EndDate` | End Date | Date | 8 | - |  |  |
| 10 | `EndTime` | End Time | Int | 11 | - |  |  |
| 11 | `ChkHash` | Checked Hash Value | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ID |
