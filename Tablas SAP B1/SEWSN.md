# SEWSN - SEWSN

- **Tabla:** SEWSN
- **Descripción:** SEWSN
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SEWSN.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `MachineNam` | Machine Name | nVarChar | 64 | - |  |  |
| 2 | `CompDbNam` | Company Db Name | nVarChar | 200 | - |  |  |
| 3 | `CollecStat` | Collection Status | Int | 11 | - | 0 | `0` = No Collection<br>`1` = In Process<br>`2` = Completed |
| 4 | `SentUser` | Sent User | nVarChar | 30 | - |  |  |
| 5 | `CompleDate` | Completion Date | nVarChar | 10 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | MachineNam, CompDbNam |
