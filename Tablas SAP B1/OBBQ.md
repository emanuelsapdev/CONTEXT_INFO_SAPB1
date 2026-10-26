# OBBQ - Item - Serial/Batch - Bin Accumulator

- **Tabla:** OBBQ
- **Descripción:** Item - Serial/Batch - Bin Accumulator
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OBBQ.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `ItemCode` | Item Code | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 3 | `SnBMDAbs` | Batch MD Internal Number | Int | 11 | [OBTN](OBTN.md) |  |  |
| 4 | `BinAbs` | Bin Internal Number | Int | 11 | [OBIN](OBIN.md) |  |  |
| 5 | `OnHandQty` | On-Hand Quantity | Num | 19.6 | - |  |  |
| 6 | `WhsCode` | Warehouse Code | nVarChar | 8 | [OWHS](OWHS.md) |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| BUSINESS_K | Yes | SnBMDAbs, BinAbs |
| BIN_ABS | No | BinAbs |
