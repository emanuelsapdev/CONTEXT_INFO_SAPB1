# SPP1 - Special Prices - Data Areas

- **Tabla:** SPP1
- **Descripción:** Special Prices - Data Areas
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SPP1.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ItemCode` | Item No. | nVarChar | 50 | [OSPP](OSPP.md) |  |  |
| 2 | `CardCode` | BP Code | nVarChar | 15 | [OSPP](OSPP.md) |  |  |
| 3 | `LINENUM` | Row Number | Int | 6 | - |  |  |
| 4 | `Price` | Special Price | Num | 19.6 | - |  |  |
| 5 | `Currency` | Price Currency | nVarChar | 3 | - |  |  |
| 6 | `Discount` | Discount % | Num | 19.6 | - |  |  |
| 7 | `ListNum` | Price List No. | Int | 6 | [OPLN](OPLN.md) | 0 |  |
| 8 | `FromDate` | Date From | Date | 8 | - |  |  |
| 9 | `ToDate` | Date To | Date | 8 | - |  |  |
| 10 | `AutoUpdt` | Auto Update | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 11 | `Expand` | Item Details | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 12 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |

## Claves e índices (4)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CardCode, ItemCode, LINENUM |
| CARD | No | CardCode |
| ITEM | No | ItemCode |
| CURRENCY | No | Currency |
