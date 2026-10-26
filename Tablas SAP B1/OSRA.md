# OSRA - Scheduled Report Actions

- **Tabla:** OSRA
- **Descripción:** Scheduled Report Actions
- **Cantidad de campos:** 40
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSRA.html

## Campos (40)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ActionCode` | Action Code | Int | 11 | - |  |  |
| 2 | `Title` | Title | nVarChar | 100 | - |  |  |
| 3 | `Notes` | Remarks | Text | 16 | - |  |  |
| 4 | `UserKey` | User | Int | 11 | [OUSR](OUSR.md) |  |  |
| 5 | `Password` | Password | nVarChar | 254 | - |  |  |
| 6 | `RunDate` | Next Run Date | Date | 8 | - |  |  |
| 7 | `RunTime` | Next Run Time | Int | 11 | - |  |  |
| 8 | `RunCounter` | Next Run Counter | Int | 11 | - | 0 |  |
| 9 | `ReportType` | Report Type | Int | 11 | - | 0 | `0` = Invalid<br>`115` = User Query<br>`857` = Sales/Purchase Analysis<br>`6000` = Inventory Valuation |
| 10 | `Active` | Schedule Active Status | VarChar | 1 | - | Y | `N` = No<br>`Y` = Yes |
| 11 | `StartDate` | Recurrence Start Date | Date | 8 | - |  |  |
| 12 | `EndType` | Recurrence End Type | VarChar | 1 | - | N | `N` = No End<br>`C` = By Counter<br>`D` = By Date |
| 13 | `EndDate` | Recurrence End Date | Date | 8 | - |  |  |
| 14 | `EndCounter` | Recurrence End Counter | Int | 11 | - | 1 |  |
| 15 | `MissBehav` | Behavior of Missed Run | VarChar | 1 | - | S | `S` = Skip<br>`R` = Run as Soon as Possible |
| 16 | `RcrType` | Recurrence Type | VarChar | 1 | - | N | `N` = None<br>`D` = Daily<br>`W` = Weekly<br>`M` = Monthly<br>`Y` = Annually |
| 17 | `RcrIntervl` | Recurrence Interval | Int | 11 | - | 1 |  |
| 18 | `RcrSubType` | Recurrence Subtype | Int | 11 | - |  |  |
| 19 | `RcrData2` | Recurrence: Additional Data 2 | Int | 11 | - |  |  |
| 20 | `RcrData1` | Recurrence: Additional Data 1 | Int | 11 | - |  |  |
| 21 | `ErrAct` | Action on Error | VarChar | 1 | - | 1 | `D` = Deactivate Immediately<br>`C` = Continue<br>`1` = Deactivate on Second Failure<br>`2` = Deactivate on Third Failure<br>`3` = Deactivate on Fourth Failure |
| 22 | `TransfXslt` | XSLT Transformation | Text | 16 | - |  |  |
| 23 | `TimeOut` | Rpt Creation Time-Out in Min. | Int | 11 | - | 5 |  |
| 24 | `MsgTitle` | Message Title | nVarChar | 254 | - |  |  |
| 25 | `MsgBody` | Message Body | nVarChar | 254 | - |  |  |
| 26 | `LicSrvr` | License Server | nVarChar | 254 | - |  |  |
| 27 | `Language` | Language | Int | 11 | - | 3 |  |
| 28 | `LstRunStat` | Last Run Status | VarChar | 1 | - | 0 | `0` = Not yet executed<br>`S` = Success<br>`T` = SAP Business One client stopped due to time-out<br>`U` = The next run date was not updated<br>`D` = Unable to distribute result<br>`X` = Unspecified failure<br>`F` = Successfully finished |
| 29 | `ErrorCount` | Number of Failed Runs | Int | 11 | - | 0 |  |
| 30 | `PrntLayout` | Print Layout | nVarChar | 20 | [RDOC](RDOC.md) |  | Do Not Print |
| 31 | `DistLstCod` | Distribution List Code | Int | 11 | [OMLS](OMLS.md) |  |  |
| 32 | `Finished` | Schedule Finished Status | VarChar | 1 | - | N |  |
| 33 | `SLDAddr` | SLD Address | nVarChar | 254 | - |  |  |
| 34 | `ObjType` | Object Type | nVarChar | 20 | - |  |  |
| 35 | `ObjAbsEnt` | Object Abs Entry | Int | 11 | - |  |  |
| 36 | `OnceAt` | Once At | Int | 11 | - |  |  |
| 37 | `Every` | Every | Int | 11 | - |  |  |
| 38 | `StartAt` | Starting At | Int | 11 | - |  |  |
| 39 | `EndAt` | Ending At | Int | 11 | - |  |  |
| 40 | `DFType` | Daily Frequency Type | VarChar | 1 | - | O | `O` = Once<br>`E` = Every<br>`D` = By Date |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ActionCode |
