# OBGS - Budget Scenario

- **Tabla:** OBGS
- **Descripción:** Budget Scenario
- **Cantidad de campos:** 16
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OBGS.html

## Campos (16)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Internal Number | Int | 11 | - |  |  |
| 2 | `Name` | Name | nVarChar | 100 | - |  |  |
| 3 | `BaseId` | Basic Budget | Int | 11 | - |  |  |
| 4 | `InitRate` | Initial Ratio Percentage | Num | 19.6 | - |  |  |
| 5 | `Locked` | Locked | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `FinancYear` | Start of Fiscal Year | Date | 8 | - |  |  |
| 7 | `IsMain` | Main | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 9 | `RoundSys` | Rounding Method | Int | 6 | - | 0 | `0` = No Rounding<br>`1` = Round to Full Decimal Amount<br>`2` = Round to Full Amount<br>`3` = Round to Full Tens Amount |
| 10 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 11 | `OcrCode` | Dimension 1 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 12 | `OcrCode2` | Dimension 2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 13 | `OcrCode3` | Dimension 3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 14 | `OcrCode4` | Dimension 4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 15 | `OcrCode5` | Dimension 5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 16 | `PrjCode` | Project Code | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId |
| SECOND | Yes | Name, FinancYear |
| INTER_KEY | No | BaseId |
