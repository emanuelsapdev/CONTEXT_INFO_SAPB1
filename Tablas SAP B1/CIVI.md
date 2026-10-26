# CIVI - IVI Config File

- **Tabla:** CIVI
- **Descripción:** IVI Config File
- **Cantidad de campos:** 16
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CIVI.html

## Campos (16)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `EnableRun` | Enable Run | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 3 | `EnblRunDt` | Enable Run Date | Date | 8 | - |  |  |
| 4 | `MsgSource` | Object ID of Message Source | Int | 11 | - |  |  |
| 5 | `IsOILMUpd` | Is OILM Updated | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 6 | `EnblDays` | Enable Valid In Days | Int | 11 | - | 30 |  |
| 7 | `LstChkMsg` | Last Checked OILM Message | Int | 11 | - |  |  |
| 8 | `LstMsgDate` | Last Build Message Date | Date | 8 | - |  |  |
| 9 | `LstHndlMsg` | Last Handled OILM Message | Int | 11 | - |  |  |
| 10 | `EnableUpd` | Enable Update | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 11 | `IgnPreUpd` | Ignore Previous Update | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 12 | `ForceRSP` | Force RSP Precheck | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 13 | `ReorderFrm` | Reorder 8.8 Messages: From Date | Date | 8 | - |  |  |
| 14 | `ReorderTo` | Reorder 8.8 Messages: To Date | Date | 8 | - |  |  |
| 15 | `InitMap` | Initialize MAP Items | VarChar | 1 | - |  |  |
| 16 | `InitStd` | Initialize STD Items | VarChar | 1 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
