# DTV9 - Datev Run Temp Data

- **Tabla:** DTV9
- **Descripción:** Datev Run Temp Data
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/DTV9.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `RunId` | Run Number | Int | 11 | [ODTV](ODTV.md) |  |  |
| 2 | `SubTaskId` | Sub Task Number | Int | 11 | - |  |  |
| 3 | `TaskType` | Sub Task Type | nVarChar | 10 | - |  |  |
| 4 | `JsForData` | Json for Converted Data | Text | 16 | - |  |  |
| 5 | `JsOKInfo` | Json for Info with OK | Text | 16 | - |  |  |
| 6 | `JsErrInfo` | Json for Info with Error | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | RunId, SubTaskId |
