# ITM1 - Items - Prices

- **Tabla:** ITM1
- **Descripción:** Items - Prices
- **Cantidad de campos:** 17
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ITM1.html

## Campos (17)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 2 | `PriceList` | Price List No. | Int | 6 | [OPLN](OPLN.md) |  |  |
| 3 | `Price` | List Price | Num | 19.6 | - |  |  |
| 4 | `Currency` | Currency for List Price | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 5 | `Ovrwritten` | Manual Price Entry | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `Factor` | Factor | Num | 19.6 | - |  |  |
| 7 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 8 | `ObjType` | Object | nVarChar | 20 | [ADP1](ADP1.md) | 4 |  |
| 9 | `AddPrice1` | Additional Price (1) | Num | 19.6 | - |  |  |
| 10 | `Currency1` | Currency for Add. Price 1 | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 11 | `AddPrice2` | Additional Price (2) | Num | 19.6 | - |  |  |
| 12 | `Currency2` | Currency for Add. Price 2 | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 13 | `Ovrwrite1` | Manual Price Entry (1) | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 14 | `Ovrwrite2` | Manual Price Entry (2) | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 15 | `BasePLNum` | Base Price List No. | Int | 6 | [OPLN](OPLN.md) |  |  |
| 16 | `UomEntry` | UoM Entry | Int | 11 | [OUOM](OUOM.md) |  |  |
| 17 | `PriceType` | Price Type | VarChar | 1 | - | M | `I` = Inventory UoM Price<br>`P` = Pricing Unit Price<br>`M` = Both I and P<br>`O` = Other UoM Price |

## Claves e índices (4)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ItemCode, PriceList |
| CURRENCY | No | Currency |
| PRICE_LIST | No | PriceList |
| MANUAL | No | Ovrwritten |
