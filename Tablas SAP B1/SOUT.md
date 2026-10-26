# SOUT - [SOUT]

- **Tabla:** SOUT
- **Descripción:** [SOUT]
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SOUT.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `LogNum` | ??' ????? | Int | 11 | - |  |  |
| 2 | `Company` | Company | nVarChar | 128 | - |  |  |
| 3 | `USER_CODE` | User code | nVarChar | 8 | - |  |  |
| 4 | `Object` | Object | Int | 11 | - |  |  |
| 5 | `ObjectAbs` | ObjectAbs | Int | 11 | - |  |  |
| 6 | `SubDate` | Submission date | Date | 8 | - |  |  |
| 7 | `SubTime` | Submission time | Int | 6 | - |  |  |
| 8 | `ActDate` | Action date | Date | 8 | - |  |  |
| 9 | `ActTime` | Action time | Int | 6 | - |  |  |
| 10 | `Status` | Status | VarChar | 1 | - | C | `C` = Check in<br>`P` = In process<br>`E` = Error<br>`S` = Success<br>`I` = Success with info |
| 11 | `ErrCode` | Error code | Int | 11 | - |  |  |
| 12 | `ErrMessage` | Error message | Text | 16 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | LogNum |
| STATUS | No | Status |
