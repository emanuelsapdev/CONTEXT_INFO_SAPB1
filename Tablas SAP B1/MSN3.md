# MSN3 - MRP Pegging Information

- **Tabla:** MSN3
- **Descripción:** MRP Pegging Information
- **Cantidad de campos:** 15
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MSN3.html

## Campos (15)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 3 | `PeriodID` | Period ID | Int | 11 | - |  |  |
| 4 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 5 | `BaseEntry` | Base Document Internal ID | Int | 11 | - |  |  |
| 6 | `BaseLine` | Base Row | Int | 11 | - |  |  |
| 7 | `BaseObj` | Base Object Type | nVarChar | 20 | - |  |  |
| 8 | `BaseDocNum` | Base Document Number | nVarChar | 16 | - |  |  |
| 9 | `BaseDue` | Base Due Date | Date | 8 | - |  |  |
| 10 | `StockType` | Stock Operation Type | VarChar | 1 | - | I | `I` = Stock Issue<br>`R` = Stock Receipt |
| 11 | `LineID` | Row Number | Int | 11 | - |  |  |
| 12 | `ParentCode` | Parent Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 13 | `StartDate` | Period Start Date | Date | 8 | - |  |  |
| 14 | `EndDate` | Period End Date | Date | 8 | - |  |  |
| 15 | `WhsCode` | Warehouse Code | nVarChar | 8 | [OWHS](OWHS.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineID |
