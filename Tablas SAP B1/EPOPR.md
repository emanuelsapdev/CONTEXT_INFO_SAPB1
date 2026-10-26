# EPOPR - EPOPR

- **Tabla:** EPOPR
- **Descripción:** EPOPR
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/EPOPR.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `SrvId` | FK to EPSRV table | Int | 11 | - |  |  |
| 2 | `OprName` | name of service operation | nVarChar | 60 | - |  |  |
| 3 | `SyncMode` | synch or a-sync mode of opr | nVarChar | 20 | - |  |  |
| 4 | `PrmMsgType` | operation parameter type | nVarChar | 60 | - |  |  |
| 5 | `PrcId` | FK to EPPRC table | nVarChar | 60 | - |  |  |
| 6 | `RetMsgType` | operation returned type | nVarChar | 60 | - |  |  |
| 7 | `ParamName` | Parameter name | nVarChar | 60 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | SrvId, OprName |
