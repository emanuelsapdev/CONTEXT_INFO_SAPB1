# AWH2 - WTax Definition - Rows2

- **Tabla:** AWH2
- **Descripción:** WTax Definition - Rows2
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AWH2.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Numerator | Int | 11 | - |  |  |
| 2 | `Code` | Tax Code | nVarChar | 4 | [OWHT](OWHT.md) |  |  |
| 3 | `EffectDate` | Date Effective | Date | 8 | - |  |  |
| 4 | `Rate` | Tax Rate | Num | 19.6 | - |  |  |
| 5 | `MinAmount` | Min. Amount | Num | 19.6 | - |  |  |
| 6 | `MaxAmount` | Max. Amount | Num | 19.6 | - |  |  |
| 7 | `WTCUR` | Progressive Tax Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 8 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 9 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 10 | `SeqNum` | Sequence Number | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code, LineNum, SeqNum, LogInstanc |
