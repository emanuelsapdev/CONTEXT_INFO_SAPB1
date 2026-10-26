# ABP2 - Branch Tributary Info. Log

- **Tabla:** ABP2
- **Descripción:** Branch Tributary Info. Log
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ABP2.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `BPLId` | BPL ID | Int | 11 | [OBPL](OBPL.md) |  |  |
| 2 | `TributID` | Tributary Info. ID | Int | 11 | - |  |  |
| 3 | `TributType` | Tributary Type | Int | 11 | [OBNI](OBNI.md) | -1 |  |
| 4 | `TTStartDat` | Tributary Type Start Date | Date | 8 | - |  |  |
| 5 | `TTEndDate` | Tributary Type End Date | Date | 8 | - |  |  |
| 6 | `TribRegCod` | Tributary Regime Code | Int | 11 | [OBNI](OBNI.md) | -1 |  |
| 7 | `TRCStartD` | Tributary Reg. Code Start Date | Date | 8 | - |  |  |
| 8 | `TRCEndDate` | Tributary Regime Code End Date | Date | 8 | - |  |  |
| 9 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 10 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 247 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | BPLId, TributID, LogInstanc |
