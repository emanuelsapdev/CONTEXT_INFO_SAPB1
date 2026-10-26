# OOPR - Opportunity

- **Tabla:** OOPR
- **Descripción:** Opportunity
- **Cantidad de campos:** 61
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OOPR.html

## Campos (61)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `OpprId` | Sequence No. | Int | 11 | - |  |  |
| 2 | `CardCode` | BP Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 3 | `SlpCode` | Main Sales Emp. | Int | 11 | [OSLP](OSLP.md) |  |  |
| 4 | `CprCode` | Contact Person | Int | 11 | [OCPR](OCPR.md) |  |  |
| 5 | `Source` | Source | Int | 11 | [OOSR](OOSR.md) |  |  |
| 6 | `IntCat1` | Interest - Field 1 | Int | 11 | [OOIN](OOIN.md) |  |  |
| 7 | `IntCat2` | Interest - Field 2 | Int | 11 | [OOIN](OOIN.md) |  |  |
| 8 | `IntCat3` | Interest - Field 3 | Int | 11 | [OOIN](OOIN.md) |  |  |
| 9 | `IntRate` | Interest Level | Int | 11 | [OOIR](OOIR.md) |  |  |
| 10 | `OpenDate` | Start Date | Date | 8 | - |  |  |
| 11 | `DifType` | Closing Type | VarChar | 1 | - | D | `M` = Months<br>`W` = Weeks<br>`D` = Days |
| 12 | `PredDate` | Predicted Closing Date | Date | 8 | - |  |  |
| 13 | `MaxSumLoc` | Local Potential Amount | Num | 19.6 | - |  |  |
| 14 | `MaxSumSys` | System Potential Amount | Num | 19.6 | - |  |  |
| 15 | `WtSumLoc` | Weighted Amount (LC) - Document | Num | 19.6 | - |  |  |
| 16 | `WtSumSys` | Weighted Amount (SC) | Num | 19.6 | - |  |  |
| 17 | `PrcnProf` | Gross Profit % | Num | 19.6 | - |  |  |
| 18 | `SumProfL` | Gross Profit Total - Local | Num | 19.6 | - |  |  |
| 19 | `SumProfS` | Gross Profit Total - System | Num | 19.6 | - |  |  |
| 20 | `Memo` | Remarks | Text | 16 | - |  |  |
| 21 | `Status` | Status | VarChar | 1 | - | O | `O` = Open<br>`L` = Lost<br>`W` = Won |
| 22 | `StatusRem` | Status Remarks | nVarChar | 30 | - |  |  |
| 23 | `Reason` | Reason for Closing | Int | 11 | [OOFR](OOFR.md) |  |  |
| 24 | `RealSumLoc` | Total Amount - Local | Num | 19.6 | - |  |  |
| 25 | `RealSumSys` | Total Amount - System | Num | 19.6 | - |  |  |
| 26 | `RealProfL` | Closing Gross Profit - Local | Num | 19.6 | - |  |  |
| 27 | `RealProfS` | Closing Gross Profit - System | Num | 19.6 | - |  |  |
| 28 | `CloPrcnt` | Closing Percentage | Num | 19.6 | - |  |  |
| 29 | `StepLast` | Current Stage No. | Int | 6 | [OOST](OOST.md) |  |  |
| 30 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 31 | `Transfered` | Transferred to next year | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 32 | `Instance` | Instance | Int | 6 | - | 0 |  |
| 33 | `CardName` | BP Name | nVarChar | 200 | - |  |  |
| 34 | `CloseDate` | Closing Date | Date | 8 | - |  |  |
| 35 | `LastSlp` | Last Sales Emp. | Int | 11 | [OSLP](OSLP.md) |  |  |
| 36 | `Name` | Opportunity Name | nVarChar | 100 | - |  |  |
| 37 | `Territory` | Territory | Int | 11 | [OTER](OTER.md) |  |  |
| 38 | `Industry` | Industry | Int | 11 | [OOND](OOND.md) |  |  |
| 39 | `ChnCrdCode` | BP Channel Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 40 | `ChnCrdName` | BP Channel Name | nVarChar | 200 | - |  |  |
| 41 | `PrjCode` | Project Code | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 42 | `CardGroup` | BP Group | Int | 6 | [OCRD](OCRD.md) |  |  |
| 43 | `ChnCrdCon` | BP Channel Contact | Int | 11 | [OCPR](OCPR.md) |  |  |
| 44 | `Owner` | Data Ownership field | Int | 11 | [OHEM](OHEM.md) |  |  |
| 45 | `attachment` | Attachments | Text | 16 | - |  |  |
| 46 | `DocType` | Linked Document Type | nVarChar | 9 | - | -1 | `-1`<br>`23` = Quotations<br>`17` = Sales Orders<br>`15` = Delivery Notes<br>`13` = Sales Invoices<br>`540000006` = Purchase Quotations<br>`22` = Purchase Orders<br>`20` = Goods Receipt POs<br>`18` = Purchase Invoices |
| 47 | `DocNum` | Linked Document Number | Int | 11 | - |  |  |
| 48 | `DocEntry` | Linked Document Entry | Int | 11 | - |  |  |
| 49 | `DocChkbox` | Document Checkbox | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 50 | `AtcEntry` | Attachment Entry | Int | 11 | - |  |  |
| 51 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 52 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 53 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 54 | `OpprType` | Opportunity Type | VarChar | 1 | - | R | `R` = Sales<br>`P` = Purchasing |
| 55 | `UpdateTS` | Update Full Time | Int | 11 | - |  |  |
| 56 | `DPPStatus` | Data Protection Status | VarChar | 1 | - | N | `N` = None<br>`D` = Erased |
| 57 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 58 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 59 | `DataVers` | Data Version | Int | 11 | - | 1 |  |
| 60 | `VersionNum` | Version Number | nVarChar | 13 | - |  |  |
| 61 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Upgrade<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Auto Summary<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year of Transfer |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | OpprId |
