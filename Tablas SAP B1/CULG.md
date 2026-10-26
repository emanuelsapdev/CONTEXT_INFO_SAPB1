# CULG - Company Upgrade Log

- **Tabla:** CULG
- **Descripción:** Company Upgrade Log
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CULG.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `LogId` | LogId | Int | 11 | - |  |  |
| 2 | `VersFrom` | Version from | Int | 11 | - |  |  |
| 3 | `VersTo` | Version to | Int | 11 | - |  |  |
| 4 | `TableId` | Table ID | nVarChar | 4 | - |  |  |
| 5 | `OnCreate` | Err. on creation | VarChar | 1 | - | C | `C` = Create<br>`Q` = Query |
| 6 | `ErrLevel` | Error Level | nVarChar | 30 | - |  |  |
| 7 | `InQuery` | - | nVarChar | 254 | - |  |  |
| 8 | `ErrMessage` | - | nVarChar | 254 | - |  |  |
| 9 | `UpgStart` | Start upgrade | nVarChar | 30 | - |  |  |
| 10 | `UserID` | User Signature | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | LogId |
