# AOCR - Distribution Rule

- **Tabla:** AOCR
- **Descripción:** Distribution Rule
- **Cantidad de campos:** 15
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AOCR.html

## Campos (15)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `OcrCode` | Factor Code | nVarChar | 8 | - |  |  |
| 2 | `OcrName` | Factor Description | nVarChar | 30 | - |  |  |
| 3 | `OcrTotal` | Total Factor | Num | 19.6 | - |  |  |
| 4 | `Direct` | Direct | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 5 | `Locked` | Locked | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 7 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 8 | `DimCode` | In Which Dimension | Int | 6 | [ODIM](ODIM.md) | 1 |  |
| 9 | `AbsEntry` | Numerator | Int | 11 | - |  |  |
| 10 | `Active` | Active | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 11 | `logInstanc` | Log Instance | Int | 11 | - |  |  |
| 12 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 13 | `updateDate` | Date of Update | Date | 8 | - |  |  |
| 14 | `IsFixedAmt` | Distribute by Fixed Amount | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 15 | `DTVId` | Datev Identifier | nVarChar | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | OcrCode, logInstanc |
