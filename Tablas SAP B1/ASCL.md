# ASCL - History

- **Tabla:** ASCL
- **Descripción:** History
- **Cantidad de campos:** 109
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ASCL.html

## Campos (109)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `callID` | Call ID | Int | 11 | - |  |  |
| 2 | `subject` | Subject | nVarChar | 254 | - |  |  |
| 3 | `customer` | Business Partner Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 4 | `custmrName` | Business Partner Name | nVarChar | 200 | - |  |  |
| 5 | `contctCode` | Contact Person | Int | 11 | [OCPR](OCPR.md) |  |  |
| 6 | `manufSN` | Mfr Serial No. | nVarChar | 36 | - |  |  |
| 7 | `internalSN` | Serial Number | nVarChar | 36 | - |  |  |
| 8 | `contractID` | Contract No. | Int | 11 | - |  |  |
| 9 | `cntrctDate` | Contract End Date | Date | 8 | - |  |  |
| 10 | `resolDate` | Resolution Date | Date | 8 | - |  |  |
| 11 | `resolTime` | Resolution Time | Int | 6 | - |  |  |
| 12 | `free_1` | Warranty | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 13 | `free_2` | Warranty End Date | Date | 8 | - |  |  |
| 14 | `origin` | Origin | Int | 6 | [OSCO](OSCO.md) |  |  |
| 15 | `itemCode` | Item Number | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 16 | `itemName` | Item Description | nVarChar | 200 | - |  |  |
| 17 | `itemGroup` | Item Group | Int | 6 | - |  |  |
| 18 | `status` | Status | Int | 6 | [OSCS](OSCS.md) | -3 |  |
| 19 | `priority` | Priority | VarChar | 1 | - | L | `L` = Low<br>`M` = Medium<br>`H` = High |
| 20 | `callType` | Call Type | Int | 6 | [OSCT](OSCT.md) |  |  |
| 21 | `problemTyp` | Problem Type | Int | 6 | [OSCP](OSCP.md) |  |  |
| 22 | `assignee` | Handled By | Int | 6 | [OUSR](OUSR.md) |  |  |
| 23 | `descrption` | Description | Text | 16 | - |  |  |
| 24 | `objType` | Object Type | nVarChar | 20 | - | 191 |  |
| 25 | `logInstanc` | Log Instance | Int | 11 | - |  |  |
| 26 | `userSign` | Creating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 27 | `createDate` | Creation Date | Date | 8 | - |  |  |
| 28 | `createTime` | Creation Time | Int | 6 | - |  |  |
| 29 | `closeDate` | Closing Date | Date | 8 | - |  |  |
| 30 | `closeTime` | Closing Time | Int | 6 | - |  |  |
| 31 | `userSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 32 | `updateDate` | Date of Update | Date | 8 | - |  |  |
| 33 | `SCL1Count` | InternalSCL1Count | Int | 11 | - | 0 |  |
| 34 | `SCL2Count` | InternalSCL2Count | Int | 11 | - | 0 |  |
| 35 | `isEntitled` | Entitled for Service | VarChar | 1 | - | N | `N` = Not Entitled<br>`C` = Valid contract exists |
| 36 | `insID` | Install Card No. | Int | 11 | [OINS](OINS.md) |  |  |
| 37 | `technician` | Technician | Int | 11 | [OHEM](OHEM.md) |  |  |
| 38 | `resolution` | Resolution | Text | 16 | - |  |  |
| 39 | `Scl1NxtLn` | SCL1 Next Line | Int | 11 | - |  |  |
| 40 | `Scl2NxtLn` | SCL2 Next Line | Int | 11 | - |  |  |
| 41 | `Scl3NxtLn` | SCL3 Next Line | Int | 11 | - |  |  |
| 42 | `Scl4NxtLn` | SCL4 Next Line | Int | 11 | - |  |  |
| 43 | `Scl5NxtLn` | SCL5 Next Line | Int | 11 | - |  |  |
| 44 | `isQueue` | Belongs to a Queue | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 45 | `Queue` | Queue | nVarChar | 20 | [OQUE](OQUE.md) |  |  |
| 46 | `resolOnDat` | Resolution on Date | Date | 8 | - |  |  |
| 47 | `resolOnTim` | Resolution on Time | Int | 6 | - |  |  |
| 48 | `respByDate` | Response by Date | Date | 8 | - |  |  |
| 49 | `respByTime` | Response by Time | Int | 6 | - |  |  |
| 50 | `respOnDate` | Response on Date | Date | 8 | - |  |  |
| 51 | `respOnTime` | Response on Time | Int | 6 | - |  |  |
| 52 | `respAssign` | Assigned for Response | Int | 6 | [OUSR](OUSR.md) |  |  |
| 53 | `AssignDate` | Assigned Date | Date | 8 | - |  |  |
| 54 | `AssignTime` | Assigned Time | Int | 6 | - |  |  |
| 55 | `UpdateTime` | Updated Time | Int | 6 | - |  |  |
| 56 | `responder` | Responder | Int | 6 | [OUSR](OUSR.md) |  |  |
| 57 | `Transfered` | Year Transfer | VarChar | 1 | - | N |  |
| 58 | `Instance` | Instance | Int | 6 | - | 0 |  |
| 59 | `DocNum` | Document Number | Int | 11 | - |  |  |
| 60 | `Series` | Series | Int | 11 | [NNM1](NNM1.md) |  |  |
| 61 | `Handwrtten` | Manual Numbering | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 62 | `PIndicator` | Period Indicator | nVarChar | 10 | [OPID](OPID.md) | ' ' |  |
| 63 | `StartDate` | Start Date | Date | 8 | - |  |  |
| 64 | `StartTime` | Start Time | Int | 11 | - |  |  |
| 65 | `EndDate` | End Date | Date | 8 | - |  |  |
| 66 | `EndTime` | End Time | Int | 11 | - |  |  |
| 67 | `Duration` | Service Call Duration | Num | 19.6 | - |  |  |
| 68 | `DurType` | Duration UoM | VarChar | 1 | - | M | `S` = Seconds<br>`M` = Minutes<br>`H` = Hours<br>`D` = Days |
| 69 | `Reminder` | Reminder | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 70 | `RemQty` | Reminder Quantity | Num | 19.6 | - |  |  |
| 71 | `RemType` | Reminder UoM | VarChar | 1 | - | M | `S` = Seconds<br>`M` = Minutes<br>`H` = Hours<br>`D` = Days |
| 72 | `RemDate` | Reminder Date | Date | 8 | - |  |  |
| 73 | `RemSent` | Reminder Sent | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 74 | `RemTime` | Reminder Time | Int | 6 | - |  |  |
| 75 | `Location` | Location | Int | 6 | [OCLO](OCLO.md) | -1 |  |
| 76 | `AddrName` | Address Name | nVarChar | 50 | - |  |  |
| 77 | `AddrType` | Address Type | VarChar | 1 | - | S | `S` = Ship To<br>`B` = Bill To |
| 78 | `Street` | Street | nVarChar | 100 | - |  |  |
| 79 | `City` | City | nVarChar | 100 | - |  |  |
| 80 | `Room` | Room | nVarChar | 50 | - |  |  |
| 81 | `State` | State | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 82 | `Country` | Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 83 | `DisplInCal` | Display in Calendar | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 84 | `SupplCode` | Supplementary Code | nVarChar | 254 | - |  |  |
| 85 | `Attachment` | Attachment | Text | 16 | - |  |  |
| 86 | `AtcEntry` | Attachment Entry | Int | 11 | - |  |  |
| 87 | `NumAtCard` | Business Partner Ref. No. | nVarChar | 200 | - |  |  |
| 88 | `ProSubType` | Problem Subtype | Int | 6 | [OPST](OPST.md) |  |  |
| 89 | `BPType` | Business Partner Type | VarChar | 1 | - | R | `R` = Sales<br>`P` = Purchasing |
| 90 | `Telephone` | Phone Number | nVarChar | 50 | - |  |  |
| 91 | `BPPhone1` | BP Phone Number1 | nVarChar | 50 | - |  |  |
| 92 | `BPPhone2` | BP Phone Number1 | nVarChar | 50 | - |  |  |
| 93 | `BPCellular` | BP Mobile Phone Number | nVarChar | 50 | - |  |  |
| 94 | `BPFax` | BP Fax Number | nVarChar | 50 | - |  |  |
| 95 | `BPShipCode` | BP Ship-to Code | nVarChar | 50 | - |  |  |
| 96 | `BPShipAddr` | BP Ship-to Address | nVarChar | 254 | - |  |  |
| 97 | `BPBillCode` | BP Bill-to Code | nVarChar | 50 | - |  |  |
| 98 | `BPBillAddr` | BP Bill-to Address | nVarChar | 254 | - |  |  |
| 99 | `BPTerrit` | Business Partner Territory | Int | 11 | - |  |  |
| 100 | `BPE_Mail` | Business Partner E-Mail | nVarChar | 100 | - |  |  |
| 101 | `BPProjCode` | Business Partner Project Code | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 102 | `BPContact` | BP Contact Person | nVarChar | 245 | - |  |  |
| 103 | `OwnerCode` | Service Call Owner | Int | 11 | [OHEM](OHEM.md) |  |  |
| 104 | `DPPStatus` | Data Protection Status | VarChar | 1 | - | N | `N` = None<br>`D` = Erased |
| 105 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 106 | `Printed` | Printed | VarChar | 1 | - | N |  |
| 107 | `DataVers` | Data Version | Int | 11 | - | 1 |  |
| 108 | `VersionNum` | Version Number | nVarChar | 13 | - |  |  |
| 109 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Upgrade<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Auto Summary<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year of Transfer |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | callID, logInstanc |
