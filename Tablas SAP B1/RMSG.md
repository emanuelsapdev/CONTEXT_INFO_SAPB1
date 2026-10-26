# RMSG - EditMode Messages

- **Tabla:** RMSG
- **Descripción:** EditMode Messages
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RMSG.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `abs` | abs | Int | 11 | - |  |  |
| 2 | `fromWho` | from Who | Int | 11 | - |  |  |
| 3 | `toWho` | to Who | Int | 11 | - |  |  |
| 4 | `date` | date | Date | 8 | - |  |  |
| 5 | `time` | time | Int | 11 | - |  |  |
| 6 | `loggedOnly` | msg valid only f logged | VarChar | 1 | - | Y |  |
| 7 | `message` | message | nVarChar | 250 | - |  |  |
| 8 | `msgRead` | was message read | VarChar | 1 | - | N |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | abs |
| TO_WHO | No | toWho |
| WHO_READ | No | toWho, msgRead |
