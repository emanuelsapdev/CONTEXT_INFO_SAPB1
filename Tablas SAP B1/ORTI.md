# ORTI - Retirement

- **Tabla:** ORTI
- **Descripción:** Retirement
- **Cantidad de campos:** 50
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ORTI.html

## Campos (50)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `DocNum` | Document Number | Int | 11 | - |  |  |
| 3 | `Series` | Series | Int | 11 | [NNM1](NNM1.md) |  |  |
| 4 | `PeriodCat` | Period Category | nVarChar | 10 | - |  |  |
| 5 | `FinncPriod` | Posting Period | Int | 11 | [OFPR](OFPR.md) |  |  |
| 6 | `PostDate` | Posting Date | Date | 8 | - |  |  |
| 7 | `DocDate` | Document Date | Date | 8 | - |  |  |
| 8 | `DocStatus` | Document Status | VarChar | 1 | - | P | `P` = Posted<br>`D` = Draft<br>`C` = Canceled |
| 9 | `TransId` | Transaction Number | Int | 11 | [OJDT](OJDT.md) |  |  |
| 10 | `Comments` | Remarks | nVarChar | 254 | - |  |  |
| 11 | `Reference` | Reference | nVarChar | 32 | - |  |  |
| 12 | `ObjType` | Object Type | nVarChar | 20 | - |  |  |
| 13 | `Currency` | Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 14 | `DocRate` | Document Rate | Num | 19.6 | - |  |  |
| 15 | `SysRate` | System Rate | Num | 19.6 | - |  |  |
| 16 | `PIndicator` | Period Indicator | nVarChar | 10 | [OPID](OPID.md) |  |  |
| 17 | `DocTotal` | Document Total | Num | 19.6 | - |  |  |
| 18 | `DocTotalFC` | Document Total (FC) | Num | 19.6 | - |  |  |
| 19 | `DocTotalSy` | Document Total (SC) | Num | 19.6 | - |  |  |
| 20 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 21 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 22 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 23 | `CreateDate` | Create Date | Date | 8 | - |  |  |
| 24 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 25 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 26 | `TransType` | Original Document | nVarChar | 20 | - | -1 | `13` = A/R Invoice<br>`19` = A/P Credit Memo<br>`18` = A/P Invoice<br>`46` = Outgoing Payment<br>`163` = A/P Correction Invoice<br>`1470000049` = Capitalization<br>`1470000060` = Fixed Assets Credit Memo<br>`-1` = All Transactions<br>`1470000075` = Manual Depreciation<br>`1470000090` = Fixed Assets Transfer<br>`1470000094` = Retirement |
| 27 | `CreatedBy` | Original | Int | 11 | - |  |  |
| 28 | `JrnlMemo` | Journal Remarks | nVarChar | 254 | - |  |  |
| 29 | `AssetDate` | Asset Value Date | Date | 8 | - |  |  |
| 30 | `CurSource` | Base Currency | VarChar | 1 | - | L | `L` = Local Currency<br>`S` = System Currency<br>`F` = Foreign Currency |
| 31 | `DocType` | Document Type | nVarChar | 15 | - | PL | `PL` = Ordinary Depreciation<br>`UP` = Unplanned Depreciation<br>`SD` = Special Depreciation<br>`AP` = Appreciation<br>`TR` = Asset Transfer<br>`NC` = Sales<br>`SC` = Scrapping<br>`TC` = Asset Class Transfer |
| 32 | `PrjSmarz` | Summarize by Project | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 33 | `DstRlSmarz` | Summarize by Distribution Rule | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 34 | `ManDprType` | Manual Depreciation Type | nVarChar | 15 | [ODTP](ODTP.md) |  |  |
| 35 | `Handwrtten` | Manual Numbering | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 36 | `CancelDate` | Cancelation Date | Date | 8 | - |  |  |
| 37 | `DprArea` | Depreciation Area | nVarChar | 15 | [ODPA](ODPA.md) |  |  |
| 38 | `BPLId` | Branch | Int | 11 | [OBPL](OBPL.md) |  |  |
| 39 | `BaseRef` | Base Reference | nVarChar | 11 | - |  |  |
| 40 | `LVARetire` | Low Value Asset Retirement | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 41 | `CancelOpt` | Cancelation Option | Int | 6 | - | 1 |  |
| 42 | `BPLName` | Branch Name | nVarChar | 200 | - |  |  |
| 43 | `VatRegNum` | VAT Reg. Number | nVarChar | 32 | - |  |  |
| 44 | `GdsMovType` | Goods Movement Type | nVarChar | 2 | - |  | `BA` = Retirement - End of Appropriation<br>`AT` = Sale or Transfer<br>`PE` = Extinction, Loss or Deterioration<br>`OT` = Other Fixed Outputs |
| 45 | `PTICode` | POI Code | nVarChar | 5 | [OPTI](OPTI.md) |  |  |
| 46 | `Letter` | Letter | VarChar | 1 | - |  |  |
| 47 | `FolNumFrom` | Folio Number From | Int | 11 | - |  |  |
| 48 | `FolNumTo` | Folio Number To | Int | 11 | - |  |  |
| 49 | `FolSeries` | Folio Series | Int | 11 | [OFNS](OFNS.md) |  |  |
| 50 | `VersionNum` | Version Number | nVarChar | 13 | - |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry |
| INDEX | Yes | DocNum, PIndicator |
| TRANS_TYPE | No | TransType, CreatedBy |
