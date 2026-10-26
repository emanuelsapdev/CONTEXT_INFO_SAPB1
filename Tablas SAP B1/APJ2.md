# APJ2 - Project Plan Steps Time Record

- **Tabla:** APJ2
- **Descripción:** Project Plan Steps Time Record
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/APJ2.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `StepCode` | Step Code | Int | 11 | - |  |  |
| 3 | `LineNum` | Line Number | Int | 11 | - |  |  |
| 4 | `Date` | Date | Date | 8 | - |  |  |
| 5 | `StartTime` | Start Time | Int | 11 | - |  |  |
| 6 | `EndTime` | End Time | Int | 11 | - |  |  |
| 7 | `Remarks` | Remarks | nVarChar | 254 | - |  |  |
| 8 | `LogInstanc` | Log Instance | Int | 11 | - |  |  |
| 9 | `Owner` | Owner | nVarChar | 254 | [OHEM](OHEM.md) |  |  |
| 10 | `Duration` | Duration | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, StepCode, LineNum, LogInstanc |
