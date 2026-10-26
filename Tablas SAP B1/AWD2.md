# AWD2 - Value Ranges

- **Tabla:** AWD2
- **Descripción:** Value Ranges
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AWD2.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [OWTD](OWTD.md) |  |  |
| 2 | `EfctFrom` | Effective From | Date | 8 | - |  |  |
| 3 | `ValueFrom` | Value From | Num | 19.6 | - |  |  |
| 4 | `Rate` | Rate | Num | 19.6 | - |  |  |
| 5 | `WTCur` | Currency | nVarChar | 3 | - |  |  |
| 6 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 7 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 8 | `SeqNum` | Sequence Number | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineNum, SeqNum, LogInstanc |
