# UILM2 - Inventory Account Substitute

- **Tabla:** UILM2
- **Descripción:** Inventory Account Substitute
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/UILM2.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `MessageID` | Message ID | Int | 11 | [OILM](OILM.md) |  |  |
| 2 | `AccountId` | Account ID | Int | 6 | - | -1 |  |
| 3 | `AcctCode` | Account Code | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 4 | `DebitCredi` | Debit or Credit | VarChar | 1 | - | U | `U` = Unknown<br>`D` = Debit<br>`C` = Credit |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | MessageID, AccountId, DebitCredi |
