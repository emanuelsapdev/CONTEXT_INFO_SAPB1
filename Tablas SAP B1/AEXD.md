# AEXD - Freight Setup

- **Tabla:** AEXD
- **Descripción:** Freight Setup
- **Cantidad de campos:** 44
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AEXD.html

## Campos (44)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ExpnsCode` | Internal Number | Int | 11 | - |  |  |
| 2 | `ExpnsName` | Name | nVarChar | 20 | - |  |  |
| 3 | `RevAcct` | Revenue Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 4 | `ExpnsAcct` | Expense Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 5 | `TaxLiable` | Tax Liable | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `RevFixSum` | Fixed Amount - Revenues | Num | 19.6 | - |  |  |
| 7 | `ExpFixSum` | Fixed Amount - Expenses | Num | 19.6 | - |  |  |
| 8 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Upgrade<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Auto Incr.<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 9 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 10 | `VatGroupI` | Output Tax Group | nVarChar | 8 | [OVTG](OVTG.md) |  |  |
| 11 | `VatGroupO` | Input Tax Group | nVarChar | 8 | [OVTG](OVTG.md) |  |  |
| 12 | `DistrbMthd` | Distribution Method | VarChar | 1 | - | N | `N` = None<br>`Q` = Quantity<br>`V` = Volume<br>`W` = Weight<br>`E` = Equally<br>`T` = Row Total |
| 13 | `In1099` | Include in 1099 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 14 | `ExpOfstAct` | Freight Clearing Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 15 | `WTLiable` | WTax Liable | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 16 | `BaseMethod` | Drawing Method | VarChar | 1 | - | T | `N` = None<br>`Q` = Quantity<br>`T` = Total<br>`A` = All |
| 17 | `Stock` | Stock | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 18 | `LstPchPrce` | Last Purchase Price | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 19 | `SalseRpt` | Sales Analysis Report | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 20 | `PchRpt` | Purchase Analysis Report | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 21 | `RevExmAcct` | Revenues Exempted Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 22 | `ExpnsExAct` | Expense Exempted Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 23 | `RevRetAct` | Revenue Returns Account | nVarChar | 15 | - |  |  |
| 24 | `ExpnsType` | Freight Type | VarChar | 1 | - |  | `1` = Shipping<br>`2` = Insurance<br>`3` = Other |
| 25 | `OcrCode` | Distribution Rule | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 26 | `TaxDisMthd` | Tax Distribution Method | VarChar | 1 | - | N | `N` = None<br>`Q` = Quantity<br>`V` = Volume<br>`W` = Weight<br>`E` = Equally<br>`T` = Row Total |
| 27 | `OcrCode2` | Distribution Rule 2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 28 | `OcrCode3` | Distribution Rule 3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 29 | `OcrCode4` | Distribution Rule 4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 30 | `OcrCode5` | Distribution Rule 5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 31 | `OcrCodeX` | Distribution Rule X | nVarChar | 100 | [OOCR](OOCR.md) |  |  |
| 32 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 33 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 34 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 35 | `Project` | Project | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 36 | `Intrastat` | Intrastat Relevant | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 37 | `GrsFreight` | Gross Freight | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 38 | `SacCode` | SAC Code | nVarChar | 8 | - |  |  |
| 39 | `FreighType` | Freight Type | VarChar | 1 | - | S | `S` = Standard<br>`B` = Bollo |
| 40 | `DataVers` | Data Version | Int | 11 | - | 1 |  |
| 41 | `DocFreight` | Document Operation Freight | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 42 | `ProdctType` | SAF-T Product Type | VarChar | 1 | - | S | `P` = Products<br>`S` = Services<br>`O` = Other<br>`I` = Taxes |
| 43 | `ProdTypeEx` | SAF-T Product Type | nVarChar | 10 | [OSPT](OSPT.md) | S |  |
| 44 | `IsActive` | Active | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ExpnsCode, LogInstanc |
