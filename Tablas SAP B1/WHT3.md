# WHT3 - Value Range

- **Tabla:** WHT3
- **Descripción:** Value Range
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WHT3.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Internal Number | Int | 11 | - |  |  |
| 2 | `WTCode` | WTax Code | nVarChar | 4 | [OWHT](OWHT.md) |  |  |
| 3 | `EfctFrom` | Effective From | Date | 8 | - |  |  |
| 4 | `ValueFrom` | Value From | Num | 19.6 | - |  |  |
| 5 | `Deduct` | WTax to Be Deductible | Num | 19.6 | - |  |  |
| 6 | `Rate` | Rate | Num | 19.6 | - |  |  |
| 7 | `WTCur` | Currency | nVarChar | 3 | - |  |  |
| 8 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 9 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 10 | `SeqNum` | Sequence Number | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WTCode, LineNum, SeqNum |
