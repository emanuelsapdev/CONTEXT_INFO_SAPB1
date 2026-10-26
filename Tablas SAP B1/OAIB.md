# OAIB - Received Alerts

- **Tabla:** OAIB
- **Descripción:** Received Alerts
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OAIB.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AlertCode` | Alert Code | Int | 11 | [OALR](OALR.md) |  |  |
| 2 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 3 | `Opened` | Opened | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 4 | `RecDate` | Receipt Date | Date | 8 | - |  |  |
| 5 | `RecTime` | Time Received | Int | 6 | - |  |  |
| 6 | `WasRead` | Read | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 7 | `Deleted` | Deleted | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `Failed` | Failed | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (4)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AlertCode, UserSign |
| USER | No | UserSign |
| READ | No | WasRead |
| DELETED | No | Deleted |
