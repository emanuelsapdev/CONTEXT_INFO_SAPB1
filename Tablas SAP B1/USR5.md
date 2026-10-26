# USR5 - User Access Log

- **Tabla:** USR5
- **Descripción:** User Access Log
- **Cantidad de campos:** 18
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/USR5.html

## Campos (18)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `UserCode` | User Code | nVarChar | 25 | [OUSR](OUSR.md) |  |  |
| 2 | `Action` | Performed Action | VarChar | 1 | - |  | `I` = Logon Succeeded<br>`F` = Logon Failed<br>`O` = Logoff<br>`C` = Created<br>`S` = Superuser Selected<br>`D` = Superuser Deselected<br>`L` = Locked<br>`U` = Unlocked<br>`P` = Password Changed<br>`N` = Screen Unlock Failed<br>`T` = Temporary User Change<br>`R` = Removed |
| 3 | `ActionBy` | User Who Performed the Action | nVarChar | 25 | - |  |  |
| 4 | `ClientIP` | IP Address of Client Computer | nVarChar | 200 | - |  |  |
| 5 | `Date` | Date | Date | 8 | - |  |  |
| 6 | `Time` | Time | Int | 11 | - | 0 |  |
| 7 | `ClientName` | Hostname of Client Computer | nVarChar | 200 | - |  |  |
| 8 | `ProcessID` | Process ID of B1 Application | Int | 11 | - | -1 |  |
| 9 | `SessionID` | Connection Session ID | Int | 11 | - | -1 |  |
| 10 | `ReasonID` | Reason ID | Int | 11 | - |  | `1` = Planned: Initial System Configuration<br>`2` = Planned: System Configuration Change<br>`3` = Planned: System Maintenance<br>`4` = Planned: Knowledge Transfer to End-User<br>`11` = Unplanned: Root Cause Analysis<br>`12` = Unplanned: Knowledge Transfer to End-User<br>`13` = Unplanned: System Maintenance<br>`14` = Unplanned: System Configuration Change<br>`51` = System Maintenance<br>`52` = Root Cause Analysis<br>`53` = Consulting / Support<br>`54` = Other |
| 11 | `ReasonDesc` | Reason Description | nVarChar | 250 | - |  |  |
| 12 | `WinSessnID` | Client Windows Session ID | Int | 11 | - | -1 |  |
| 13 | `WinUsrName` | User Name of Windows User | nVarChar | 100 | - |  |  |
| 14 | `ProcName` | Process Name of Logged-On App. | nVarChar | 80 | - |  |  |
| 15 | `AliveDurtn` | Time Logged-On User Keep Alive | Int | 11 | - | 0 |  |
| 16 | `LogoutTime` | User Logout Time | Int | 11 | - |  |  |
| 17 | `Source` | Login Terminal | nVarChar | 100 | - |  |  |
| 18 | `UserID` | User ID | Int | 6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | UserCode, Action, Date, Time, SessionID |
