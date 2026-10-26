# AITT - Product Tree - History

- **Tabla:** AITT
- **Descripción:** Product Tree - History
- **Cantidad de campos:** 29
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AITT.html

## Campos (29)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Parent Item | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 2 | `TreeType` | BOM Type | VarChar | 1 | - | P | `A` = Assembly<br>`S` = Sales<br>`P` = Production<br>`T` = Template |
| 3 | `PriceList` | Price List | Int | 6 | [OPLN](OPLN.md) | 0 |  |
| 4 | `Qauntity` | No. of Units | Num | 19.6 | - |  |  |
| 5 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 6 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 7 | `Transfered` | Postponed to Next Year | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `DataSource` | Data source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 9 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 10 | `SCNCounter` | SCN Counter | Int | 6 | - |  |  |
| 11 | `DispCurr` | Display Currency | nVarChar | 3 | - |  |  |
| 12 | `ToWH` | Whse for Finished Product | nVarChar | 8 | - |  |  |
| 13 | `Object` | Object Type | nVarChar | 20 | - | 66 |  |
| 14 | `LogInstac` | Log Instance - History | Int | 11 | - |  |  |
| 15 | `UserSign2` | Updating User | Int | 11 | [OUSR](OUSR.md) |  |  |
| 16 | `OcrCode` | Distribution Rule | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 17 | `HideComp` | Hide Components in Printing | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 18 | `OcrCode2` | Distribution Rule2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 19 | `OcrCode3` | Distribution Rule3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 20 | `OcrCode4` | Distribution Rule4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 21 | `OcrCode5` | Distribution Rule5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 22 | `UpdateTime` | Time of Update | Int | 11 | - |  |  |
| 23 | `Project` | Project Code | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 24 | `PlAvgSize` | Planned Average Production Size | Num | 19.6 | - | 1 |  |
| 25 | `Name` | Product Description | nVarChar | 200 | - |  |  |
| 26 | `CreateTS` | Create Time - Incl. Secs | Int | 11 | - |  |  |
| 27 | `UpdateTS` | Update Full Time | Int | 11 | - |  |  |
| 28 | `AtcEntry` | Attachment Entry | Int | 11 | [OATC](OATC.md) |  |  |
| 29 | `Attachment` | Attachments | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code, LogInstac |
