# SWEI - SWEI

- **Tabla:** SWEI
- **Descripción:** SWEI
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SWEI.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `EngineAddr` | Workflow Engine Address | nVarChar | 200 | - |  |  |
| 2 | `EngineVer` | Workflow Engine Version | nVarChar | 30 | - |  |  |
| 3 | `HashCode` | Random Generated Hash Code | Int | 11 | - |  |  |
| 4 | `StartTime` | Start Date of Workflow Engine | nVarChar | 50 | - |  |  |
| 5 | `LastUpdate` | Last Update Date and Time | nVarChar | 50 | - |  |  |
| 6 | `NextUpdate` | Expected next update date | nVarChar | 50 | - |  |  |
| 7 | `EngCmpnys` | Company dbs that support workf | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | EngineAddr |
