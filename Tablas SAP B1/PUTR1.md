# PUTR1 - Pre-Upgrade Test Result Line

- **Tabla:** PUTR1
- **Descripción:** Pre-Upgrade Test Result Line
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/PUTR1.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `SerialNum` | Serial Number | Int | 11 | - |  |  |
| 2 | `TestID` | Test ID | Int | 11 | - |  |  |
| 3 | `TestDesc` | Test Description | nVarChar | 254 | - |  |  |
| 4 | `Result` | Result | VarChar | 1 | - |  | `S` = Success<br>`E` = Error<br>`W` = Warning<br>`K` = Skipped |
| 5 | `BeginTime` | Start Time | nVarChar | 20 | - |  |  |
| 6 | `EndTime` | End Time | nVarChar | 20 | - |  |  |
| 7 | `SAPNote` | SAP Note Link | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | SerialNum, TestID |
