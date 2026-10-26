# OFTP - Microsoft 365 Integration Doc. Export

- **Tabla:** OFTP
- **Descripción:** Microsoft 365 Integration Doc. Export
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OFTP.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TASKID` | Task ID | nVarChar | 254 | - |  |  |
| 2 | `USER_ID` | User Id | nVarChar | 254 | - |  |  |
| 3 | `CURR` | Current | Int | 11 | - |  |  |
| 4 | `TOTAL` | Total | Int | 11 | - |  |  |
| 5 | `ERROR_CODE` | Error Code | nVarChar | 254 | - |  |  |
| 6 | `STATE` | State | nVarChar | 254 | - |  |  |
| 7 | `STARTTIME` | Start Time | Date | 8 | - |  |  |
| 8 | `FILE_NAME` | File Name | nVarChar | 254 | - |  |  |
| 9 | `RESULT` | Result | Text | 16 | - |  |  |
| 10 | `ONETTOKEN` | One Time Token | Text | 16 | - |  |  |
| 11 | `TASKTYPE` | Task Type | nVarChar | 254 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TASKID |
