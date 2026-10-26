# RLOG - Resource Edit Log

- **Tabla:** RLOG
- **Descripción:** Resource Edit Log
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RLOG.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsKey` | Abs Key | Int | 11 | - |  |  |
| 2 | `UserSign` | User Sign | Int | 11 | - |  |  |
| 3 | `ResType` | Resource Type | Int | 11 | - |  |  |
| 4 | `MasterKey` | Master Key | nVarChar | 64 | - |  |  |
| 5 | `SlaveNum` | Slave Num | nVarChar | 20 | - |  |  |
| 6 | `Date` | Date | Date | 8 | - |  |  |
| 7 | `Time` | Time | Int | 6 | - |  |  |
| 8 | `FldName` | Field Name | nVarChar | 10 | - |  |  |
| 9 | `NewVal` | New Value | nVarChar | 64 | - |  |  |
| 10 | `BatchNum` | Batch Change Number | Int | 11 | - |  |  |
| 11 | `ResCode` | Resource Code | Int | 11 | - | -1 |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsKey, ResCode |
| RESOURCE | No | ResType, MasterKey, SlaveNum |
| USER | No | UserSign |
