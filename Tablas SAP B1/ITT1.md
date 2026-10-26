# ITT1 - Bill of Materials - Components

- **Tabla:** ITT1
- **Descripción:** Bill of Materials - Components
- **Cantidad de campos:** 29
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ITT1.html

## Campos (29)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Father` | Parent Item | nVarChar | 50 | [OITT](OITT.md) |  |  |
| 2 | `ChildNum` | Component Element Number | Int | 11 | - |  |  |
| 3 | `VisOrder` | Visual Order | Int | 11 | - |  |  |
| 4 | `Code` | Component Code | nVarChar | 50 | - |  |  |
| 5 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 6 | `Warehouse` | Warehouse | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 7 | `Price` | Price | Num | 19.6 | - |  |  |
| 8 | `Currency` | Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 9 | `PriceList` | Price List | Int | 6 | [OPLN](OPLN.md) | 0 |  |
| 10 | `OrigPrice` | Original Price | Num | 19.6 | - |  |  |
| 11 | `OrigCurr` | Original Currency | nVarChar | 3 | - |  |  |
| 12 | `IssueMthd` | Issue Method | VarChar | 1 | - |  | `B` = Backflush<br>`M` = Manual |
| 13 | `Uom` | Inventory UoM | nVarChar | 100 | - |  |  |
| 14 | `Comment` | Comment | nVarChar | 254 | - |  |  |
| 15 | `LogInstanc` | Log Instance | Int | 11 | - |  |  |
| 16 | `Object` | Object | nVarChar | 20 | - | 66 |  |
| 17 | `OcrCode` | Distribution Rule | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 18 | `OcrCode2` | Distribution Rule2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 19 | `OcrCode3` | Distribution Rule3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 20 | `OcrCode4` | Distribution Rule4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 21 | `OcrCode5` | Distribution Rule5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 22 | `PrncpInput` | Principal Input | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 23 | `Project` | Project Code | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 24 | `Type` | Component Type | Int | 11 | - | 4 | `4` = Item<br>`290` = Resource<br>`-18` = Text |
| 25 | `WipActCode` | WIP Account Code | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 26 | `AddQuantit` | Additional Quantity | Num | 19.6 | - |  |  |
| 27 | `LineText` | Row Text | Text | 16 | - |  |  |
| 28 | `StageId` | Stage ID | Int | 11 | - |  |  |
| 29 | `ItemName` | Item Description | nVarChar | 200 | - |  |  |

## Claves e índices (5)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Father, ChildNum |
| VISORDER | Yes | Father, VisOrder |
| FATHER | No | Father |
| CHILD | No | Code |
| PRICE_LIST | No | PriceList |
