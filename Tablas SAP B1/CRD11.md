# CRD11 - BP Tributary Info.

- **Tabla:** CRD11
- **Descripción:** BP Tributary Info.
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CRD11.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CardCode` | BP Code | nVarChar | 25 | [OCRD](OCRD.md) |  |  |
| 2 | `Address` | Address | nVarChar | 50 | - |  |  |
| 3 | `TributID` | Tributary Info. ID | Int | 11 | - |  |  |
| 4 | `TributType` | Tributary Type | Int | 11 | [OBNI](OBNI.md) | -1 |  |
| 5 | `TTStartDat` | Tributary Type Start Date | Date | 8 | - |  |  |
| 6 | `TTEndDate` | Tributary Type End Date | Date | 8 | - |  |  |
| 7 | `TribRegCod` | Tributary Regime Code | Int | 11 | [OBNI](OBNI.md) | -1 |  |
| 8 | `TRCStartD` | Tributary Reg. Code Start Date | Date | 8 | - |  |  |
| 9 | `TRCEndDate` | Tributary Regime Code End Date | Date | 8 | - |  |  |
| 10 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CardCode, Address, TributID |
