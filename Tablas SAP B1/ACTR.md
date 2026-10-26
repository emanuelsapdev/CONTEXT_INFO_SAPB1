# ACTR - Service Contracts

- **Tabla:** ACTR
- **Descripción:** Service Contracts
- **Cantidad de campos:** 70
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ACTR.html

## Campos (70)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ContractID` | Contract No. | Int | 11 | - |  |  |
| 2 | `CstmrCode` | Business Partner Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 3 | `CstmrName` | Business Partner Name | nVarChar | 200 | - |  |  |
| 4 | `CntctCode` | Contact Person Code | Int | 11 | [OCPR](OCPR.md) |  |  |
| 5 | `Owner` | Owner | Int | 6 | [OUSR](OUSR.md) |  |  |
| 6 | `Status` | Contract Status | VarChar | 1 | - | D | `A` = Approved<br>`F` = On Hold<br>`D` = Draft<br>`T` = Terminated |
| 7 | `CntrcTmplt` | Contract Template | nVarChar | 20 | [OCTT](OCTT.md) |  |  |
| 8 | `CntrcType` | Contract Type | VarChar | 1 | - | S | `C` = Business Partner<br>`G` = Item Group<br>`S` = Serial Number |
| 9 | `Renewal` | Renewal | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 10 | `RemindVal` | Reminder Time | Int | 6 | - |  |  |
| 11 | `RemindUnit` | Remind Unit | VarChar | 1 | - | D | `D` = Days<br>`W` = Weeks<br>`M` = Months |
| 12 | `Duration` | Duration of Coverage | Int | 6 | - |  |  |
| 13 | `StartDate` | Start Date | Date | 8 | - |  |  |
| 14 | `EndDate` | End Date | Date | 8 | - |  |  |
| 15 | `ResponsVal` | Resolution Time | Int | 6 | - |  |  |
| 16 | `ResponsUnt` | Resolution Unit | VarChar | 1 | - | D | `D` = Days<br>`H` = Hours |
| 17 | `Descriptio` | Description | nVarChar | 254 | - |  |  |
| 18 | `SrcDocType` | Source Document Type | VarChar | 1 | - | I | `Q` = Sales Quotation<br>`O` = Sales Order<br>`D` = Delivery<br>`I` = A/R Invoice |
| 19 | `DocNum` | Source Document | Int | 11 | - |  |  |
| 20 | `MonEnabled` | Monday Enabled | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 21 | `TueEnabled` | Tuesday Enabled | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 22 | `WedEnabled` | Wednesday Enabled | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 23 | `ThuEnabled` | Thursday Enabled | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 24 | `FriEnabled` | Friday Enabled | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 25 | `SatEnabled` | Saturday Enabled | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 26 | `SunEnabled` | Sunday Enabled | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 27 | `MonStart` | Monday Start | Int | 6 | - | 800 |  |
| 28 | `MonEnd` | Monday End | Int | 6 | - | 1700 |  |
| 29 | `TueStart` | Tuesday Start | Int | 6 | - | 800 |  |
| 30 | `TueEnd` | Tuesday End | Int | 6 | - | 1700 |  |
| 31 | `WedStart` | Wednesday Start | Int | 6 | - | 800 |  |
| 32 | `WedEnd` | Wednesday End | Int | 6 | - | 1700 |  |
| 33 | `ThuStart` | Thursday Start | Int | 6 | - | 800 |  |
| 34 | `ThuEnd` | Thursday End | Int | 6 | - | 1700 |  |
| 35 | `FriStart` | Friday Start | Int | 6 | - | 800 |  |
| 36 | `FriEnd` | Friday End | Int | 6 | - | 1700 |  |
| 37 | `SatStart` | Saturday Start | Int | 6 | - | 0 |  |
| 38 | `SatEnd` | Saturday End | Int | 6 | - | 2359 |  |
| 39 | `SunStrart` | Sunday Start | Int | 6 | - | 0 |  |
| 40 | `SunEnd` | Sunday End | Int | 6 | - | 2359 |  |
| 41 | `InclParts` | Include Parts | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 42 | `InclWork` | Include Labor | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 43 | `InclTravel` | Include Travel | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 44 | `Attachment` | Attachments | Text | 16 | - |  |  |
| 45 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 46 | `Remarks1` | Template Remarks | Text | 16 | - |  |  |
| 47 | `Remarks2` | Remarks | Text | 16 | - |  |  |
| 48 | `RemindFlg` | Reminder Sent | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 49 | `CTR1Count` | CTR1 Counter | Int | 11 | - | 0 |  |
| 50 | `DocEntry` | Linked Document No. | Int | 11 | - |  |  |
| 51 | `RemTmDays` | Remind Time in Days | Int | 11 | - |  |  |
| 52 | `ResTmHours` | Response Time in Hours | Int | 11 | - |  |  |
| 53 | `InclHldays` | Include Holidays | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 54 | `SrvcType` | Service Type | VarChar | 1 | - | R | `R` = Regular<br>`W` = Warranty |
| 55 | `TermDate` | Termination Date | Date | 8 | - |  |  |
| 56 | `ResponseV` | Response Time | Int | 6 | - |  |  |
| 57 | `ResponseU` | Response Unit | VarChar | 1 | - | H | `D` = Days<br>`H` = Hours |
| 58 | `AtcEntry` | Attachment Entry | Int | 11 | [OATC](OATC.md) |  |  |
| 59 | `Transfered` | Year Transfer | VarChar | 1 | - | N |  |
| 60 | `Instance` | Instance | Int | 6 | - | 0 |  |
| 61 | `BPType` | BP Type | VarChar | 1 | - | R | `R` = Sales<br>`P` = Purchasing |
| 62 | `OwnerCode` | Service Contract Owner | Int | 11 | [OHEM](OHEM.md) |  |  |
| 63 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 64 | `ObjType` | Object Type - History | nVarChar | 20 | - | 190 |  |
| 65 | `LogInstanc` | Log Instance - History | Int | 11 | - |  |  |
| 66 | `UserSign2` | Updating User - History | Int | 6 | [OUSR](OUSR.md) |  |  |
| 67 | `UpdateDate` | Date of Update - History | Date | 8 | - |  |  |
| 68 | `DPPStatus` | Data Protection Status | VarChar | 1 | - | N | `N` = None<br>`D` = Erased |
| 69 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 70 | `Printed` | Printed | VarChar | 1 | - | N |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ContractID, LogInstanc |
