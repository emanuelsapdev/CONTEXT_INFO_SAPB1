# FCT1 - Sales Forecast - Rows

- **Tabla:** FCT1
- **Descripción:** Sales Forecast - Rows
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/FCT1.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsID` | Internal Number | Int | 11 | [OFCT](OFCT.md) |  |  |
| 2 | `LineID` | Row Number | Int | 11 | - |  |  |
| 3 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 4 | `Date` | Day Forecasted | Date | 8 | - |  |  |
| 5 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 6 | `WhsCode` | Warehouse | nVarChar | 8 | [OWHS](OWHS.md) | -1 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsID, ItemCode, Date, WhsCode |
