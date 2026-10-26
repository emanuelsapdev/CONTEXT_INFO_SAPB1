# DPS1 - Deposit - Rows

- **Tabla:** DPS1
- **Descripción:** Deposit - Rows
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/DPS1.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DepositId` | Deposit Key | Int | 11 | [ODPS](ODPS.md) |  |  |
| 2 | `CheckKey` | Check Key | Int | 11 | - |  |  |
| 3 | `DepCancel` | Canceled | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DepositId, CheckKey |
