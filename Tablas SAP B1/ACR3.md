# ACR3 - Business Partner Control Accounts - History

- **Tabla:** ACR3
- **Descripción:** Business Partner Control Accounts - History
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ACR3.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CardCode` | BP Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 2 | `AcctType` | Account Type | VarChar | 1 | - | M | `M` = Domestic<br>`F` = Foreign<br>`D` = Down Payment<br>`A` = Assets Account<br>`R` = Bill of Exchange Accounts Receivable<br>`P` = Bill of Exchange Accounts Payable<br>`C` = Bill of Exchange on Collection<br>`S` = Bill of Exchange Presentation<br>`Y` = Assets Bill of Exchange Acct Payable<br>`I` = Bill of Exchange Discounted<br>`U` = Unpaid Bill of Exchange<br>`O` = Open Debts |
| 3 | `AcctCode` | Account Code | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 4 | `LogInstane` | Log Instance | Int | 11 | - | 0 |  |
| 5 | `ObjType` | Object Type | Int | 6 | [ADP1](ADP1.md) | 2 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CardCode, AcctType, LogInstane |
