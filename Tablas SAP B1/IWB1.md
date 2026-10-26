# IWB1 - Batch No. Quantities Backup

- **Tabla:** IWB1
- **Descripción:** Batch No. Quantities Backup
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/IWB1.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Abs. Entry | Int | 11 | [OIWB](OIWB.md) |  |  |
| 2 | `LineNumber` | Line Number | Int | 11 | - |  |  |
| 3 | `BtqAbs` | Btq Abs. Entry | Int | 11 | [OBTQ](OBTQ.md) |  |  |
| 4 | `MdAbsEntry` | MD Abs. Entry | Int | 11 | [OBTN](OBTN.md) |  |  |
| 5 | `CountedQty` | Counted Quantity | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineNumber |
