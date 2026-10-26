# OCLG - Activities

- **Tabla:** OCLG
- **Descripción:** Activities
- **Cantidad de campos:** 99
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCLG.html

## Campos (99)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ClgCode` | Activity Number | Int | 11 | - |  |  |
| 2 | `CardCode` | BP Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 3 | `Notes` | Remarks | Text | 16 | - |  |  |
| 4 | `CntctDate` | System Date | Date | 8 | - |  |  |
| 5 | `CntctTime` | Time | Int | 11 | - |  |  |
| 6 | `Recontact` | Activity Date | Date | 8 | - |  |  |
| 7 | `Closed` | Closed Activity | VarChar | 1 | - | N | `Y` = Closed<br>`N` = Open |
| 8 | `CloseDate` | Closing Date | Date | 8 | - |  |  |
| 9 | `ContactPer` | Contact Person Name | nVarChar | 90 | - |  |  |
| 10 | `Tel` | Telephone | nVarChar | 50 | - |  |  |
| 11 | `Fax` | Fax | nVarChar | 50 | - |  |  |
| 12 | `CntctSbjct` | Activity Subject | Int | 6 | [OCLS](OCLS.md) | -1 |  |
| 13 | `Transfered` | Transfered to Next Year | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 14 | `DocType` | Linked Document | nVarChar | 20 | - | -1 | `13` = A/R Invoice<br>`14` = A/R Credit Memo<br>`15` = Delivery<br>`16` = Return<br>`17` = Sales Order<br>`18` = A/P Invoice<br>`19` = A/P Credit Memo<br>`20` = Goods Receipt PO<br>`21` = Goods Return<br>`22` = Purchase Order<br>`23` = Sales Quotation<br>`24` = Incoming Payment<br>`25` = Deposit<br>`30` = Journal Entry<br>`46` = Outgoing Payment<br>`57` = Checks for Payment<br>`59` = Goods Receipt<br>`60` = Goods Issue<br>`1250000001` = Inventory Transfer Request<br>`67` = Inventory Transfer<br>`68` = Work Order<br>`69` = Landed Costs<br>`132` = Correction Invoice<br>`162` = Material Revaluation<br>`202` = Production Order<br>`203` = A/R Down Payment<br>`204` = A/P Down Payment<br>`140000009` = Outgoing Excise Invoice<br>`140000010` = Incoming Excise Invoice<br>`-1`<br>`0`<br>`4` = Items<br>`163` = A/P Correction Invoice<br>`164` = A/P Correction Invoice Reversal<br>`165` = A/R Correction Invoice<br>`166` = A/R Correction Invoice Reversal<br>`1320000012` = Campaign<br>`540000006` = Purchase Quotation<br>`1250000025` = Blanket Agreements<br>`1470000113` = Purchase Request<br>`112` = Document Drafts<br>`140` = Payment Drafts<br>`123` = Checks for Payment Drafts<br>`254000065` = Self Invoice<br>`254000066` = Self Credit Memo<br>`234000031` = Return Request<br>`234000032` = Goods Return Request<br>`1250000026` = Sales Blanket Agreement<br>`1250000027` = Purchasing Blanket Agreement |
| 15 | `DocNum` | Linked Document Number | nVarChar | 50 | - |  |  |
| 16 | `DocEntry` | Linked Document Entry | nVarChar | 50 | - |  |  |
| 17 | `Attachment` | Attachment | Text | 16 | - |  |  |
| 18 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 19 | `AttendUser` | Dealt by | Int | 6 | [OUSR](OUSR.md) |  |  |
| 20 | `CntctCode` | Contact Person | Int | 11 | [OCPR](OCPR.md) |  |  |
| 21 | `UserSign` | User Signature | Int | 6 | - |  |  |
| 22 | `SlpCode` | Sales Employee | Int | 11 | [OSLP](OSLP.md) | -1 |  |
| 23 | `Action` | Activity | VarChar | 1 | - | C | `C` = Phone Call<br>`M` = Meeting<br>`T` = Task<br>`L` = E-Mail<br>`E` = Note<br>`P` = Campaign<br>`N` = Other |
| 24 | `Details` | Details | nVarChar | 100 | - |  |  |
| 25 | `CntctType` | Activity Type | Int | 6 | [OCLT](OCLT.md) | -1 |  |
| 26 | `Location` | Location | Int | 6 | [OCLO](OCLO.md) | -1 |  |
| 27 | `BeginTime` | Start Time | Int | 11 | - |  |  |
| 28 | `Duration` | Activity Duration | Num | 19.6 | - |  |  |
| 29 | `DurType` | Duration UoM | VarChar | 1 | - | M | `S` = Seconds<br>`M` = Minutes<br>`H` = Hours<br>`D` = Days |
| 30 | `ENDTime` | End Time | Int | 11 | - |  |  |
| 31 | `Priority` | Priority | VarChar | 1 | - | 1 | `0` = Low<br>`1` = Normal<br>`2` = High |
| 32 | `Reminder` | Reminder | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 33 | `RemQty` | Reminder Quantity | Num | 19.6 | - |  |  |
| 34 | `RemType` | Reminder Units | VarChar | 1 | - | M | `S` = Seconds<br>`M` = Minutes<br>`H` = Hours<br>`D` = Days |
| 35 | `OprId` | Opportunity - Key | Int | 11 | - |  |  |
| 36 | `OprLine` | Row No. - Opportunity | Int | 6 | - |  |  |
| 37 | `RemDate` | Reminder Date | Date | 8 | - |  |  |
| 38 | `RemTime` | Reminder Time | Int | 6 | - |  |  |
| 39 | `RemSented` | Reminder Was Sent | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 40 | `Instance` | Instance | Int | 6 | - | 0 |  |
| 41 | `endDate` | End/Due Date | Date | 8 | - |  |  |
| 42 | `status` | Status | Int | 11 | [OCLA](OCLA.md) |  |  |
| 43 | `personal` | Personal Flag | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 44 | `inactive` | Inactive Flag | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 45 | `emailed` | Emailed Flag | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 46 | `tentative` | Tentative Flag | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 47 | `street` | Street | nVarChar | 100 | - |  |  |
| 48 | `city` | City | nVarChar | 100 | - |  |  |
| 49 | `country` | Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 50 | `state` | State | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 51 | `room` | Room | nVarChar | 50 | - |  |  |
| 52 | `parentType` | Parent Object Type | nVarChar | 20 | - |  | `97` = Opportunity<br>`191` = Service Call |
| 53 | `parentId` | Parent Object ID | Int | 11 | - |  |  |
| 54 | `prevActvty` | Previous Activity | Int | 11 | - |  |  |
| 55 | `AtcEntry` | Attachment Entry | Int | 11 | - |  |  |
| 56 | `RecurPat` | Recurrence Pattern | VarChar | 1 | - | N | `N` = None<br>`D` = Daily<br>`W` = Weekly<br>`M` = Monthly<br>`A` = Annually |
| 57 | `EndType` | Recurrence End Type | VarChar | 1 | - | N | `N` = No End Date<br>`C` = By Counter<br>`D` = By Date |
| 58 | `SeStartDat` | Series Start Date | Date | 8 | - |  |  |
| 59 | `SeEndDat` | Series End Date | Date | 8 | - |  |  |
| 60 | `MaxOccur` | Max Occurrences | Int | 11 | - |  |  |
| 61 | `Interval` | Interval | Int | 11 | - | 1 |  |
| 62 | `Sunday` | Sunday | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 63 | `Monday` | Monday | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 64 | `Tuesday` | Tuesday | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 65 | `Wednesday` | Wednesday | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 66 | `Thursday` | Thursday | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 67 | `Friday` | Friday | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 68 | `Saturday` | Saturday | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 69 | `SubOption` | Suboption | VarChar | 1 | - | 1 | `1` = Option 1<br>`2` = Option 2 |
| 70 | `DayInMonth` | Repeat Day in Month | Int | 11 | - |  |  |
| 71 | `Month` | Repeat Month | Int | 11 | - |  |  |
| 72 | `DayOfWeek` | Repeat Day of Week | Int | 11 | - |  |  |
| 73 | `Week` | Repeat Week in Month | Int | 11 | - |  | `1` = first<br>`2` = second<br>`3` = third<br>`4` = fourth<br>`5` = last |
| 74 | `SeriesNum` | Series Number | Int | 11 | - |  |  |
| 75 | `OrigDate` | Original Date | Date | 8 | - |  |  |
| 76 | `IsRemoved` | Removed Flag | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 77 | `LastRemind` | Last Reminder Date | Date | 8 | - |  |  |
| 78 | `AssignedBy` | Assigned By | Int | 6 | [OUSR](OUSR.md) |  |  |
| 79 | `AddrName` | Address Name | nVarChar | 50 | - |  |  |
| 80 | `AddrType` | Address Type | VarChar | 1 | - | S | `S` = Ship To<br>`B` = Bill To |
| 81 | `AttendEmpl` | Dealt by Employee | Int | 11 | [OHEM](OHEM.md) |  |  |
| 82 | `NextDate` | Date of Next Occurrence | Date | 8 | - |  |  |
| 83 | `NextTime` | Time of Next Occurrence | Int | 6 | - |  |  |
| 84 | `OwnerCode` | Activities Owner | Int | 11 | [OHEM](OHEM.md) |  |  |
| 85 | `AttendReci` | Attend Recipient | Int | 11 | [ORCI](ORCI.md) |  |  |
| 86 | `ActType` | Activity Type | Int | 11 | [PMC5](PMC5.md) |  |  |
| 87 | `LaborItem` | Labor Item No. | nVarChar | 50 | - |  |  |
| 88 | `ResCode` | Resource Code from ORSC | nVarChar | 50 | [ORSC](ORSC.md) |  |  |
| 89 | `FIPROJECT` | Financial Project | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 90 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 91 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 92 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 93 | `DPPStatus` | Data Protection Status | VarChar | 1 | - | N | `N` = None<br>`D` = Erased |
| 94 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 95 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 96 | `DataVers` | Data Version | Int | 11 | - | 1 |  |
| 97 | `Of365EvtId` | Office 365 Event ID | nVarChar | 200 | - |  |  |
| 98 | `AssigneeTy` | Assignee Type | Int | 11 | - | 12 | `12` = User<br>`171` = Employee<br>`234000033` = Recipient List<br>`-1` = Multiple Recipients |
| 99 | `VersionNum` | Version Number | nVarChar | 13 | - |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ClgCode |
| CRD_CODE | No | CardCode |
| OPPORT | No | OprId, OprLine |
