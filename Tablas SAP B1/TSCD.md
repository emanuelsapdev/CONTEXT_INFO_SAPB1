# TSCD - Schedules

- **Tabla:** TSCD
- **Descripción:** Schedules
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TSCD.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `SrvcName` | Service application name | nVarChar | 20 | - |  |  |
| 2 | `SchedType` | Type of schedule | VarChar | 1 | - | P | `P` = Suspended / Paused<br>`O` = Once<br>`S` = Every X seconds<br>`M` = Every X minutes<br>`D` = Daily<br>`W` = Weekly<br>`T` = Monthly |
| 3 | `SchedDate` | Scheduled date | Date | 8 | - |  |  |
| 4 | `SchedDay` | Scheduled day | nVarChar | 2 | - | 1 |  |
| 5 | `Interval` | Interval | Int | 11 | - |  |  |
| 6 | `LastExDate` | Last execution date | Date | 8 | - |  |  |
| 7 | `AutoStart` | Auto run when OS starts | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = NO |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | SrvcName |
| NAME_SCHED | Yes | SrvcName, LastExDate |
