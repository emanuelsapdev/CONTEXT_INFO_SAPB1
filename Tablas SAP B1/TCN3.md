# TCN3 - Tracking Note - Warehouse Qty

- **Tabla:** TCN3
- **Descripción:** Tracking Note - Warehouse Qty
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TCN3.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Abs. Entry | Int | 11 | [OTCN](OTCN.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `WhsCode` | Warehouse Code | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 4 | `QtyOnHand` | On Hand Quantity | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineNum, WhsCode |
