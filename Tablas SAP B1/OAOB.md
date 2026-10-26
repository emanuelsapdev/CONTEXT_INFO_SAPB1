# OAOB - Message Sent

- **Tabla:** OAOB
- **Descripción:** Message Sent
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OAOB.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AlertCode` | Alert Code | Int | 11 | [OALR](OALR.md) |  |  |
| 2 | `SendDate` | Date | Date | 8 | - |  |  |
| 3 | `SendTime` | Time | Int | 6 | - |  |  |
| 4 | `WasSent` | Sent | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 5 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AlertCode, UserSign |
| USER | No | UserSign |
