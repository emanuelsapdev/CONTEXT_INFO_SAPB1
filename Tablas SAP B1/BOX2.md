# BOX2 - Box Definition - Accounts

- **Tabla:** BOX2
- **Descripción:** Box Definition - Accounts
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/BOX2.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `BoxCode` | Group Code | nVarChar | 30 | - |  |  |
| 2 | `ReportType` | Report Type | VarChar | 1 | - | B | `B`<br>`S` |
| 3 | `Account` | Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 4 | `SeqNum` | Sequence Number | Int | 11 | - |  |  |
| 5 | `EffecDate` | Effective From | Date | 8 | - |  |  |
| 6 | `BosCode` | Box Set Code | Int | 11 | [OBOS](OBOS.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | BoxCode, ReportType, BosCode, Account |
