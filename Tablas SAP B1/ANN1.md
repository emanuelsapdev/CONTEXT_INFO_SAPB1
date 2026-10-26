# ANN1 - Documents Numbering - Series - History

- **Tabla:** ANN1
- **Descripción:** Documents Numbering - Series - History
- **Cantidad de campos:** 39
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ANN1.html

## Campos (39)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ObjectCode` | Document | nVarChar | 20 | [ONNM](ONNM.md) |  |  |
| 2 | `Series` | Series | Int | 11 | - | 0 |  |
| 3 | `SeriesName` | Series Name | nVarChar | 8 | - |  |  |
| 4 | `InitialNum` | Initial Number | Int | 11 | - | 0 |  |
| 5 | `NextNumber` | Next Number for Use | Int | 11 | - | 0 |  |
| 6 | `LastNum` | Last Number Allowed | Int | 11 | - |  |  |
| 7 | `BeginStr` | Prefix String | nVarChar | 20 | - |  |  |
| 8 | `EndStr` | Suffix String | nVarChar | 20 | - |  |  |
| 9 | `Remark` | Remarks | nVarChar | 50 | - |  |  |
| 10 | `GroupCode` | Group | Int | 6 | - | 1 | `1` = Series Group 1<br>`2` = Series Group 2<br>`3` = Series Group 3<br>`4` = Series Group 4<br>`5` = Series Group 5<br>`6` = Series Group 6<br>`7` = Series Group 7<br>`8` = Series Group 8<br>`9` = Series Group 9<br>`10` = Series Group 10<br>`11` = Series Group 11<br>`12` = Series Group 12<br>`13` = Series Group 13<br>`14` = Series Group 14<br>`15` = Series Group 15<br>`16` = Series Group 16<br>`17` = Series Group 17<br>`18` = Series Group 18<br>`19` = Series Group 19<br>`20` = Series Group 20<br>`21` = Series Group 21<br>`22` = Series Group 22<br>`23` = Series Group 23<br>`24` = Series Group 24<br>`25` = Series Group 25<br>`26` = Series Group 26<br>`27` = Series Group 27<br>`28` = Series Group 28<br>`29` = Series Group 29<br>`30` = Series Group 30 |
| 11 | `Locked` | Locked | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 12 | `YearTransf` | Year-End Closing | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 13 | `Indicator` | Period Indicator | nVarChar | 10 | [OPID](OPID.md) | ' ' |  |
| 14 | `Template` | Template | nVarChar | 20 | - |  |  |
| 15 | `NumSize` | Numeric Size | Int | 11 | - |  |  |
| 16 | `FolioPref` | Folio Prefix String | nVarChar | 4 | - |  |  |
| 17 | `NextFolio` | Next Folio Number | Int | 11 | - |  |  |
| 18 | `DocSubType` | Document Sub-Type | nVarChar | 2 | - | -- |  |
| 19 | `DefESeries` | Default Electronic Series | Int | 6 | - | 0 |  |
| 20 | `IsDigSerie` | Is Digital Series | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 21 | `SeriesType` | Series Type | VarChar | 1 | - | D | `D` = Document<br>`B` = Business Partner<br>`I` = Item<br>`R` = Resource<br>`W` = Withholding Certificates |
| 22 | `IsManual` | Is Manual Series | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 23 | `BPLId` | Assigned Branch | Int | 11 | [OBPL](OBPL.md) |  |  |
| 24 | `IsForCncl` | Is Series for Cancellation | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 25 | `AtDocType` | AT Document Type | nVarChar | 10 | - |  |  |
| 26 | `IsElAuth` | Electronic Authorization Code | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 27 | `CoAccount` | Cost Account Only | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 28 | `GenPassprt` | Do Generate SAP Passport | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 29 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 30 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 31 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 32 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 33 | `logInstanc` | Log Instance - History | Int | 11 | - |  |  |
| 34 | `PInvType` | Abs Type of Positive Value Invoice | Int | 11 | [OEIT](OEIT.md) |  |  |
| 35 | `NInvType` | Abs Type of Negative Value Invoice | Int | 11 | [OEIT](OEIT.md) |  |  |
| 36 | `AssignedID` | Assigned ID | nVarChar | 70 | - |  |  |
| 37 | `Action` | Action | VarChar | 1 | - |  | `R` = Report<br>`C` = Cancel<br>`F` = Finalize |
| 38 | `Status` | Status | VarChar | 1 | - |  | `R` = Reported<br>`C` = Canceled<br>`F` = Finalized |
| 39 | `Phase` | Phase | VarChar | 1 | - |  | `T` = To Be Processed<br>`I` = In Process<br>`O` = OK<br>`E` = Error |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Series, logInstanc |
