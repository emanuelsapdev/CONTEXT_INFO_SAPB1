# LIVI - IVI Log File

- **Tabla:** LIVI
- **Descripción:** IVI Log File
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/LIVI.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `LogEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `Version` | B1 Main Version | Int | 11 | - |  |  |
| 3 | `PatchLevel` | B1 PL Version | nVarChar | 50 | - |  |  |
| 4 | `Comment` | Recalculation Comment | nVarChar | 100 | - |  |  |
| 5 | `LoadCustom` | Load customs from OIPF | VarChar | 1 | - | Y | `N` = No<br>`Y` = Yes |
| 6 | `LastMsgID` | Last OILM Message ID | Int | 11 | - |  |  |
| 7 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 8 | `InitMap` | Initialize MAP Items | VarChar | 1 | - |  |  |
| 9 | `InitStd` | Initialize STD Items | VarChar | 1 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | LogEntry |
