# EMERR - EMERR

- **Tabla:** EMERR
- **Descripción:** EMERR
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/EMERR.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ID` | Error ID | Identity | 11 | - |  |  |
| 2 | `QueueType` | Queue type | nVarChar | 30 | - |  |  |
| 3 | `IDInQueue` | Message ID in the queue | nVarChar | 60 | - |  |  |
| 4 | `ErrCode` | Error code | nVarChar | 60 | - |  |  |
| 5 | `Severity` | Error severity | nVarChar | 10 | - |  |  |
| 6 | `ErrMessage` | Error message | nVarChar | 254 | - |  |  |
| 7 | `Member` | Error accessed member | nVarChar | 60 | - |  |  |
| 8 | `ExcType` | Exception type | nVarChar | 160 | - |  |  |
| 9 | `ExcString` | Exception string | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ID |
