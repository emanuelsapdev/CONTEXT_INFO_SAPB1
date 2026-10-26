# FTR2 - Transfer - Area Journal Transactions

- **Tabla:** FTR2
- **Descripción:** Transfer - Area Journal Transactions
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/FTR2.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | [OFTR](OFTR.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `DprArea` | Depreciation Area | nVarChar | 15 | [ODPA](ODPA.md) |  |  |
| 4 | `JrnlMemo` | Journal Remarks | nVarChar | 254 | - |  |  |
| 5 | `ObjType` | Object Type | nVarChar | 20 | - |  |  |
| 6 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 7 | `TransNum` | Transaction Number | Int | 11 | [OJDT](OJDT.md) |  |  |
| 8 | `JrnlMemo1` | Cancellation Journal Remarks | nVarChar | 254 | - |  |  |
| 9 | `TransNum1` | Cancellation Transaction No. | Int | 11 | [OJDT](OJDT.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum |
