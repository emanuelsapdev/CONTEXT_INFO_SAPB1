# OCYC - Cycle

- **Tabla:** OCYC
- **Descripción:** Cycle
- **Cantidad de campos:** 24
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCYC.html

## Campos (24)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Cycle Code | Int | 6 | - |  |  |
| 2 | `Name` | Cycle Name | nVarChar | 20 | - |  |  |
| 3 | `Frequency` | Frequency | VarChar | 1 | - |  | `0` = Daily<br>`1` = Weekly<br>`2` = Every Four Weeks<br>`3` = Monthly<br>`4` = Quarterly<br>`5` = Semiannually<br>`6` = Annually<br>`7` = None<br>`8` = Every "X" Days: |
| 4 | `Day` | Day | Int | 11 | - |  |  |
| 5 | `Hour` | Hour | Int | 11 | - |  |  |
| 6 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 7 | `NextDate` | Next Counting Date | Date | 8 | - |  |  |
| 8 | `Type` | Cycle Type | VarChar | 1 | - | C | `C` = Cycle<br>`M` = MRP |
| 9 | `SubOption` | Suboption | VarChar | 1 | - | 1 | `1` = Option 1<br>`2` = Option 2 |
| 10 | `Interval` | Interval | Int | 11 | - | 1 |  |
| 11 | `EndType` | Recurrence End Type | VarChar | 1 | - | N | `N` = No End Date<br>`C` = By Counter<br>`D` = By Date |
| 12 | `MaxOccur` | Max. Occurrences | Int | 11 | - |  |  |
| 13 | `SeEndDat` | Series End Date | Date | 8 | - |  |  |
| 14 | `Sunday` | Sunday | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 15 | `Monday` | Monday | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 16 | `Tuesday` | Tuesday | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 17 | `Wednesday` | Wednesday | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 18 | `Thursday` | Thursday | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 19 | `Friday` | Friday | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 20 | `Saturday` | Saturday | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 21 | `DayInMonth` | Repeat Day in Month | Int | 11 | - |  |  |
| 22 | `Week` | Repeat Week in Month | Int | 11 | - |  | `1` = First<br>`2` = Second<br>`3` = Third<br>`4` = Fourth<br>`5` = Last |
| 23 | `DayOfWeek` | Repeat Day of Week | Int | 11 | - |  | `8` = Day<br>`9` = Weekday<br>`0` = Weekend Day<br>`1` = Sunday<br>`2` = Monday<br>`3` = Tuesday<br>`4` = Wednesday<br>`5` = Thursday<br>`6` = Friday<br>`7` = Saturday |
| 24 | `Month` | Repeat Month | Int | 11 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code |
| NAME | Yes | Name |
