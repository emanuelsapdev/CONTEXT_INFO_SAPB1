# AUOM - UoM Master Data

- **Tabla:** AUOM
- **Descripción:** UoM Master Data
- **Cantidad de campos:** 34
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AUOM.html

## Campos (34)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `UomEntry` | UoM Abs. Entry | Int | 11 | - |  |  |
| 2 | `UomCode` | UoM Code | nVarChar | 20 | - |  |  |
| 3 | `UomName` | UoM Name | nVarChar | 100 | - |  |  |
| 4 | `Locked` | Locked | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 5 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 6 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 7 | `LogInstanc` | Log Instance | Int | 6 | - | 0 |  |
| 8 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 9 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 10 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 11 | `Length1` | Length 1 | Num | 19.6 | - |  |  |
| 12 | `Len1Unit` | Unit of Length 1 | Int | 6 | - |  |  |
| 13 | `length2` | Length 2 | Num | 19.6 | - |  |  |
| 14 | `Len2Unit` | Unit of Length 2 | Int | 6 | - |  |  |
| 15 | `Width1` | Width 1 | Num | 19.6 | - |  |  |
| 16 | `Wdth1Unit` | Unit of Width 1 | Int | 6 | - |  |  |
| 17 | `Width2` | Width 2 | Num | 19.6 | - |  |  |
| 18 | `Wdth2Unit` | Unit of Width 2 | Int | 6 | - |  |  |
| 19 | `Height1` | Height 1 | Num | 19.6 | - |  |  |
| 20 | `Hght1Unit` | Unit of Height 1 | Int | 6 | - |  |  |
| 21 | `Height2` | Height 2 | Num | 19.6 | - |  |  |
| 22 | `Hght2Unit` | Unit of Height 2 | Int | 6 | - |  |  |
| 23 | `Volume` | Volume | Num | 19.6 | - |  |  |
| 24 | `VolUnit` | Volume UoM | Int | 6 | - |  |  |
| 25 | `Weight1` | Weight 1 | Num | 19.6 | - |  |  |
| 26 | `WghtUnit` | Weight UoM | Int | 6 | - |  |  |
| 27 | `Weight2` | Weight 2 | Num | 19.6 | - |  |  |
| 28 | `Wght2Unit` | Unit of Weight 2 | Int | 6 | - |  |  |
| 29 | `IntSymbol` | International Symbol | nVarChar | 20 | - |  |  |
| 30 | `EwbUnit` | EWB Unit | Int | 11 | [OEUT](OEUT.md) |  |  |
| 31 | `PPWeight1` | Plastic Packaging Weight 1 | Num | 19.6 | - |  |  |
| 32 | `PPWe1Unit` | Plastic Packaging Weight 1 Unit | Int | 6 | - |  |  |
| 33 | `PPWeight2` | Plastic Packaging Weight 2 | Num | 19.6 | - |  |  |
| 34 | `PPWe2Unit` | Plastic Packaging Weight 2 Unit | Int | 6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | UomEntry, LogInstanc |
