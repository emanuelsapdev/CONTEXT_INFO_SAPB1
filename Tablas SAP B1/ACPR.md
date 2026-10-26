# ACPR - Contact Persons - History

- **Tabla:** ACPR
- **Descripción:** Contact Persons - History
- **Cantidad de campos:** 57
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ACPR.html

## Campos (57)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CntctCode` | Internal Number | Int | 11 | - |  |  |
| 2 | `CardCode` | BP Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 3 | `Name` | Contact Person Name | nVarChar | 50 | - |  |  |
| 4 | `Position` | Position | nVarChar | 90 | - |  |  |
| 5 | `Address` | Address | nVarChar | 254 | - |  |  |
| 6 | `Tel1` | Telephone 1 | nVarChar | 50 | - |  |  |
| 7 | `Tel2` | Telephone 2 | nVarChar | 50 | - |  |  |
| 8 | `Cellolar` | Mobile Phone Number | nVarChar | 50 | - |  |  |
| 9 | `Fax` | Fax Number | nVarChar | 50 | - |  |  |
| 10 | `E_MailL` | E-Mail | nVarChar | 100 | - |  |  |
| 11 | `Pager` | Pager | nVarChar | 30 | - |  |  |
| 12 | `Notes1` | Remark 1 | nVarChar | 100 | - |  |  |
| 13 | `Notes2` | Remark 2 | nVarChar | 100 | - |  |  |
| 14 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 15 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 16 | `Password` | Password | nVarChar | 8 | - |  |  |
| 17 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 18 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) |  |  |
| 19 | `BirthPlace` | Place of Birth | nVarChar | 100 | - |  |  |
| 20 | `BirthDate` | Date of Birth | Date | 8 | - |  |  |
| 21 | `Gender` | Gender | VarChar | 1 | - | E | `M` = Male<br>`F` = Female<br>`E`<br>`*` = Masked<br>`I` = Not Valid for System |
| 22 | `Profession` | Profession | nVarChar | 50 | - |  |  |
| 23 | `updateDate` | Date of Update | Date | 8 | - |  |  |
| 24 | `updateTime` | Update Time | Int | 11 | - |  |  |
| 25 | `Title` | Title | nVarChar | 10 | - |  |  |
| 26 | `BirthCity` | City of Birth | nVarChar | 100 | - |  |  |
| 27 | `Active` | Active | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 28 | `FirstName` | First Name | nVarChar | 50 | - |  |  |
| 29 | `MiddleName` | Middle Name | nVarChar | 50 | - |  |  |
| 30 | `LastName` | Last Name | nVarChar | 50 | - |  |  |
| 31 | `BirthState` | State of Birth | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 32 | `ResidCity` | City of Residence | nVarChar | 100 | - |  |  |
| 33 | `ResidCntry` | Country/Region of Residence | nVarChar | 100 | - |  |  |
| 34 | `ResidState` | State of Residence | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 35 | `NFeRcpn` | NF-e Recipient | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 36 | `EmlGrpCode` | E-Mail Group Code | nVarChar | 20 | [OEGP](OEGP.md) |  |  |
| 37 | `BlockComm` | Block Sending Marketing | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 38 | `FiscalCode` | Fiscal Code for Resident | nVarChar | 16 | - |  |  |
| 39 | `CtyPrvsYr` | City for Previous Year | nVarChar | 100 | - |  |  |
| 40 | `SttPrvsYr` | State for Previous Year | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 41 | `CtyCdPrvsY` | City Code for Previous Year | nVarChar | 4 | - |  |  |
| 42 | `CtyCurYr` | City for Current Year | nVarChar | 100 | - |  |  |
| 43 | `SttCurYr` | State for Current Year | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 44 | `CtyCdCurYr` | City Code for Current Year | nVarChar | 4 | - |  |  |
| 45 | `NotResdSch` | Not resident Schumacker | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 46 | `CtyFsnCode` | Fusione comuni | nVarChar | 100 | - |  |  |
| 47 | `NaturalPer` | Natural Person | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 48 | `DPPStatus` | Data Protection Status | VarChar | 1 | - | N | `N` = None<br>`D` = Erased<br>`B` = Blocked<br>`U` = Unblocked |
| 49 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 50 | `CreateTS` | Creation Time Incl. Sec. | Int | 11 | - |  |  |
| 51 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 52 | `CnnectAddr` | Connected Address | nVarChar | 50 | - |  |  |
| 53 | `CnAddrType` | Connected Address Type | VarChar | 1 | - |  | `S` = Ship To<br>`B` = Bill To |
| 54 | `Frgncntry` | Stato Estero | nVarChar | 3 | - |  |  |
| 55 | `EnGender` | Encryption of Gender | Text | 16 | - |  |  |
| 56 | `GenderEx` | Gender | nVarChar | 15 | [OGDR](OGDR.md) | E |  |
| 57 | `EnGenderEx` | Encryption of GenderEx | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CntctCode, LogInstanc |
