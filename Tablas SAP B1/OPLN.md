# OPLN - Price Lists

- **Tabla:** OPLN
- **Descripción:** Price Lists
- **Cantidad de campos:** 24
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OPLN.html

## Campos (24)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ListNum` | Price List No. | Int | 6 | - |  |  |
| 2 | `ListName` | Price List Name | nVarChar | 32 | - |  |  |
| 3 | `BASE_NUM` | Base Price List | Int | 6 | [OPLN](OPLN.md) |  |  |
| 4 | `Factor` | Factor | Num | 19.6 | - |  |  |
| 5 | `RoundSys` | Rounding Method | Int | 6 | - | 0 | `0` = No Rounding<br>`1` = Round to Full Decimal Amount<br>`2` = Round to Full Amount<br>`3` = Round to Full Tens Amount<br>`4` = Fixed Ending<br>`5` = Fixed Interval |
| 6 | `GroupCode` | Group No. | Int | 6 | - | 1 | `1` = Price List - Group No. 1<br>`2` = Price List - Group No. 2<br>`3` = Price List - Group No. 3<br>`4` = Price List - Group No. 4<br>`5` = Price List - Group No. 5<br>`6` = Price List - Group No. 6<br>`7` = Price List - Group No. 7<br>`8` = Price List - Group No. 8<br>`9` = Price List - Group No. 9<br>`10` = Price List - Group No. 10<br>`11` = Price List - Group No. 11<br>`12` = Price List - Group No. 12<br>`13` = Price List - Group No. 13<br>`14` = Price List - Group No. 14<br>`15` = Price List - Group No. 15<br>`16` = Price List - Group No. 16<br>`17` = Price List - Group No. 17<br>`18` = Price List - Group No. 18<br>`19` = Price List - Group No. 19<br>`20` = Price List - Group No. 20<br>`21` = Price List - Group No. 21<br>`22` = Price List - Group No. 22<br>`23` = Price List - Group No. 23<br>`24` = Price List - Group No. 24<br>`25` = Price List - Group No. 25<br>`26` = Price List - Group No. 26<br>`27` = Price List - Group No. 27<br>`28` = Price List - Group No. 28<br>`29` = Price List - Group No. 29<br>`30` = Price List - Group No. 30 |
| 7 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 8 | `SPPCounter` | SPP Counter | Int | 11 | - |  |  |
| 9 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 10 | `IsGrossPrc` | Gross Price? | VarChar | 1 | - | N | `Y` = Gross<br>`N` = Net |
| 11 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 12 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 13 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 14 | `ValidFor` | Active | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 15 | `ValidFrom` | Active From | Date | 8 | - |  |  |
| 16 | `ValidTo` | Active To | Date | 8 | - |  |  |
| 17 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 18 | `PrimCurr` | Primary Default Currency | nVarChar | 3 | - |  |  |
| 19 | `AddCurr1` | Additional Default Currency 1 | nVarChar | 3 | - |  |  |
| 20 | `AddCurr2` | Additional Default Currency 2 | nVarChar | 3 | - |  |  |
| 21 | `RoundRule` | Rounding Rule | VarChar | 1 | - | R | `R` = Round to Closest<br>`C` = Round Up<br>`F` = Round Down |
| 22 | `ExtAmount` | Fixed Amount (Ending/Interval) | Num | 19.6 | - |  |  |
| 23 | `RndFrmtInt` | Ending/Interval - Integer Part | nVarChar | 10 | - |  |  |
| 24 | `RndFrmtDec` | Ending/Interval - Decimal Part | nVarChar | 10 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ListNum |
| LIST_NAME | Yes | ListName |
