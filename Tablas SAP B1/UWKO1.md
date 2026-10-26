# UWKO1 - Production Instructions - Rows

- **Tabla:** UWKO1
- **Descripción:** Production Instructions - Rows
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/UWKO1.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `OrderNum` | Instruction Key | Int | 11 | [OWKO](OWKO.md) |  |  |
| 2 | `LineID` | Row Number | Int | 11 | - | 0 |  |
| 3 | `ItemCode` | Item No. | nVarChar | 50 | [OITT](OITT.md) |  |  |
| 4 | `Descript` | Item Description | nVarChar | 200 | - |  |  |
| 5 | `Quantity` | Item Quantity | Num | 19.6 | - |  |  |
| 6 | `Price` | Item Price | Num | 19.6 | - |  |  |
| 7 | `Currency` | Price Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 8 | `WhsCode` | Item Warehouse | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 9 | `FinncPriod` | Posting Period | Int | 11 | [OFPR](OFPR.md) |  |  |
| 10 | `ActWorkCod` | Active Account Code | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 11 | `ActWorkSum` | Total Work | Num | 19.6 | - |  |  |
| 12 | `ProdUpgNum` | Production Upgrade No. | Int | 11 | [OWOR](OWOR.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | OrderNum, LineID |
| CURRENCY | No | Currency |
