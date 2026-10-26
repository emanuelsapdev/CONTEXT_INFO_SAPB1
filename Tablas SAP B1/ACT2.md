# ACT2 - Service Contract - Recurring Transactions

- **Tabla:** ACT2
- **Descripción:** Service Contract - Recurring Transactions
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ACT2.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ContractID` | Contract No. | Int | 11 | [OCTR](OCTR.md) |  |  |
| 2 | `RcpEntry` | Recurring Template Entry | Int | 11 | [ORCP](ORCP.md) |  |  |
| 3 | `LogInstanc` | Log Instance - History | Int | 11 | - |  |  |
| 4 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ContractID, RcpEntry, LogInstanc |
