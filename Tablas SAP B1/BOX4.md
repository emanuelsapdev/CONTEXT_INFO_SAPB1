# BOX4 - Box Definition - Contra Accounts of Accounts

- **Tabla:** BOX4
- **Descripción:** Box Definition - Contra Accounts of Accounts
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/BOX4.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ReportType` | Report Type | VarChar | 1 | - | B | `B`<br>`S` |
| 2 | `EffecDate` | Effective From | Date | 8 | - |  |  |
| 3 | `BoxCode` | Group Code | nVarChar | 30 | - |  |  |
| 4 | `Account` | Account | nVarChar | 15 | - |  |  |
| 5 | `ContraAct` | Offset Account | nVarChar | 15 | - |  |  |
| 6 | `SeqNum` | Sequence Number | Int | 11 | - |  |  |
| 7 | `BosCode` | Box Set Code | Int | 11 | [OBOS](OBOS.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | BoxCode, ReportType, BosCode, Account, ContraAct |
