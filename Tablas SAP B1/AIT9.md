# AIT9 - Item - UoM Prices

- **Tabla:** AIT9
- **Descripción:** Item - UoM Prices
- **Cantidad de campos:** 17
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AIT9.html

## Campos (17)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 2 | `PriceList` | Price List No. | Int | 6 | [OPLN](OPLN.md) |  |  |
| 3 | `UomEntry` | UoM Entry | Int | 11 | [OUOM](OUOM.md) |  |  |
| 4 | `Factor` | Reduced By % | Num | 19.6 | - |  |  |
| 5 | `Price` | UoM Price | Num | 19.6 | - |  |  |
| 6 | `Currency` | Currency for UoM Price | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 7 | `AutoUpdate` | Automatic Update | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 8 | `AddPrice1` | Additional Price (1) | Num | 19.6 | - |  |  |
| 9 | `Currency1` | Currency for Add. Price 1 | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 10 | `AddPrice2` | Additional Price (2) | Num | 19.6 | - |  |  |
| 11 | `Currency2` | Currency for Add. Price 2 | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 12 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 13 | `ObjType` | Object | nVarChar | 20 | [ADP1](ADP1.md) | 4 |  |
| 14 | `Factor1` | Reduced By % | Num | 19.6 | - |  |  |
| 15 | `Factor2` | Reduced By % | Num | 19.6 | - |  |  |
| 16 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 17 | `PriceType` | Price Type | VarChar | 1 | - | O | `I` = Inventory UoM Price<br>`P` = Pricing Unit Price<br>`M` = Both I and P<br>`O` = Other UoM Price |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ItemCode, PriceList, UomEntry, LogInstanc |
