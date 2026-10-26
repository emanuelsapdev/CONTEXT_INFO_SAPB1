# AHEM - Employees - History

- **Tabla:** AHEM
- **Descripción:** Employees - History
- **Cantidad de campos:** 141
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AHEM.html

## Campos (141)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `empID` | Employee No. | Int | 11 | - |  |  |
| 2 | `lastName` | Last Name | nVarChar | 50 | - |  |  |
| 3 | `firstName` | First Name | nVarChar | 50 | - |  |  |
| 4 | `middleName` | Middle Name | nVarChar | 50 | - |  |  |
| 5 | `sex` | Gender | VarChar | 1 | - | M | `F` = Female<br>`M` = Male<br>`E` = Not Specified<br>`*` = Masked<br>`I` = Not Valid for System |
| 6 | `jobTitle` | Job Title | nVarChar | 20 | - |  |  |
| 7 | `type` | Employee Type | Int | 11 | [OHTY](OHTY.md) |  |  |
| 8 | `dept` | Department | Int | 6 | [OUDP](OUDP.md) |  |  |
| 9 | `branch` | Branch | Int | 6 | [OUBR](OUBR.md) |  |  |
| 10 | `workStreet` | Work Street | nVarChar | 100 | - |  |  |
| 11 | `workBlock` | Work Block | nVarChar | 100 | - |  |  |
| 12 | `workZip` | Work Zip Code | nVarChar | 20 | - |  |  |
| 13 | `workCity` | Work City | nVarChar | 100 | - |  |  |
| 14 | `workCounty` | Work County | nVarChar | 100 | - |  |  |
| 15 | `workCountr` | Work Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 16 | `workState` | Work State | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 17 | `manager` | Manager | Int | 11 | [OHEM](OHEM.md) |  |  |
| 18 | `userId` | User ID | Int | 11 | [OUSR](OUSR.md) |  |  |
| 19 | `salesPrson` | Sales Employee | Int | 11 | [OSLP](OSLP.md) |  |  |
| 20 | `officeTel` | Office Phone | nVarChar | 50 | - |  |  |
| 21 | `officeExt` | Office Ext. | nVarChar | 50 | - |  |  |
| 22 | `mobile` | Mobile Phone | nVarChar | 50 | - |  |  |
| 23 | `pager` | Pager | nVarChar | 50 | - |  |  |
| 24 | `homeTel` | Home Phone | nVarChar | 50 | - |  |  |
| 25 | `fax` | Fax | nVarChar | 50 | - |  |  |
| 26 | `email` | E-Mail | nVarChar | 100 | - |  |  |
| 27 | `startDate` | Start Date | Date | 8 | - |  |  |
| 28 | `status` | Status | Int | 11 | [OHST](OHST.md) |  |  |
| 29 | `salary` | Salary | Num | 19.6 | - |  |  |
| 30 | `salaryUnit` | Salary Unit | VarChar | 1 | - | M | `H` = Hour<br>`D` = Day<br>`W` = Week<br>`M` = Month<br>`Y` = Year<br>`S` = Semimonthly<br>`B` = Biweekly |
| 31 | `emplCost` | Employee Costs | Num | 19.6 | - |  |  |
| 32 | `empCostUnt` | Employee Cost Unit | VarChar | 1 | - | M | `H` = Hour<br>`D` = Day<br>`W` = Week<br>`M` = Month<br>`Y` = Year |
| 33 | `termDate` | Termination Date | Date | 8 | - |  |  |
| 34 | `termReason` | Termination Reason | Int | 11 | [OHTR](OHTR.md) |  |  |
| 35 | `bankCode` | Bank Code | nVarChar | 30 | [ODSC](ODSC.md) |  |  |
| 36 | `bankBranch` | Bank Branch | nVarChar | 100 | - |  |  |
| 37 | `bankBranNo` | Bank Branch No. | nVarChar | 30 | - |  |  |
| 38 | `bankAcount` | Bank Account | nVarChar | 100 | - |  |  |
| 39 | `homeStreet` | Home Street | nVarChar | 100 | - |  |  |
| 40 | `homeBlock` | Home Block | nVarChar | 100 | - |  |  |
| 41 | `homeZip` | Home Zip Code | nVarChar | 20 | - |  |  |
| 42 | `homeCity` | Home City | nVarChar | 100 | - |  |  |
| 43 | `homeCounty` | Home County | nVarChar | 100 | - |  |  |
| 44 | `homeCountr` | Home Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 45 | `homeState` | Home State | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 46 | `birthDate` | Date of Birth | Date | 8 | - |  |  |
| 47 | `brthCountr` | Country/Region of Birth | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 48 | `martStatus` | Marital Status | VarChar | 1 | - | S | `S` = Single<br>`M` = Married<br>`D` = Divorced<br>`W` = Widowed<br>`N` = Not Specified |
| 49 | `nChildren` | No. of Children | Int | 6 | - |  |  |
| 50 | `govID` | ID Issued by Authorities | nVarChar | 64 | - |  |  |
| 51 | `citizenshp` | Citizenship | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 52 | `passportNo` | Passport No. | nVarChar | 64 | - |  |  |
| 53 | `passportEx` | Passport Expiration Date | Date | 8 | - |  |  |
| 54 | `picture` | Picture | nVarChar | 200 | - |  |  |
| 55 | `remark` | Remarks | Text | 16 | - |  |  |
| 56 | `attachment` | Attachments | Text | 16 | - |  |  |
| 57 | `salaryCurr` | Salary Currency | nVarChar | 3 | - |  |  |
| 58 | `empCostCur` | Employee Costs Currency | nVarChar | 3 | - |  |  |
| 59 | `WorkBuild` | Work Building/Floor/Room | Text | 16 | - |  |  |
| 60 | `HomeBuild` | Home Building/Floor/Room | Text | 16 | - |  |  |
| 61 | `position` | Position | Int | 11 | [OHPS](OHPS.md) |  |  |
| 62 | `AtcEntry` | Attachment Entry | Int | 11 | - |  |  |
| 63 | `AddrTypeW` | Work Address Type | nVarChar | 100 | - |  |  |
| 64 | `AddrTypeH` | Home Address Type | nVarChar | 100 | - |  |  |
| 65 | `StreetNoW` | Work Street No. | nVarChar | 100 | - |  |  |
| 66 | `StreetNoH` | Home Street No. | nVarChar | 100 | - |  |  |
| 67 | `DispMidNam` | Display Middle Name | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 68 | `NamePos` | Name Positioning Set | VarChar | 1 | - | 1 | `1` = Last Name, First Name<br>`2` = First Name, Last Name |
| 69 | `DispComma` | Display Comma | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 70 | `CostCenter` | Cost Center | nVarChar | 8 | [OPRC](OPRC.md) |  |  |
| 71 | `CompanyNum` | Company Number | nVarChar | 20 | - |  |  |
| 72 | `VacPreYear` | Vacation: Previous Year | Int | 11 | - |  |  |
| 73 | `VacCurYear` | Vacation: Current Year | Int | 11 | - |  |  |
| 74 | `MunKey` | Municipality Key | nVarChar | 20 | - |  |  |
| 75 | `TaxClass` | Tax Class | nVarChar | 2 | - | 0 | `0`<br>`1` = Tax Class I<br>`2` = Tax Class II<br>`3` = Tax Class III<br>`4` = Tax Class IV<br>`5` = Tax Class V<br>`6` = Tax Class VI |
| 76 | `InTaxLiabi` | Income Tax Liability | nVarChar | 2 | - | 0 | `0`<br>`1` = On Tax Card<br>`2` = Flat-Rate Tax<br>`3` = Cross-Border Employee<br>`4` = Not Liable |
| 77 | `EmTaxCCode` | Religion | nVarChar | 9 | - | 0 | `0`<br>`--` = No Church Tax Liability<br>`AK` = (AK) Old Catholic<br>`EV` = (EV) Protestant<br>`FA` = (FA) Non-Denomination Alzey<br>`FB` = (FB) Non-Denominational Regional Congregation Baden<br>`FG` = (FG) Non-Denominational Regional Congregation Palatinate<br>`FM` = (FM) Non-Denominational Congregation Mainz<br>`FR` = (FR) French-Reformed<br>`FS` = (FS) Non-Denominational Congregation Offenbach/Mainz<br>`IB` = (IB) Israelite Religious Community Baden<br>`IL` = (IL) Israelite Rural<br>`IS` = (IS) Israelite<br>`IW` = (IW) Israelite Religious Community Wuerttemberg<br>`JD` = (JD) Jewish Religion Tax<br>`JH` = (JH) Jewish Religion Tax<br>`JS` = (JS) Jewish Religion Tax<br>`LT` = (LT) Lutheran<br>`RF` = (RF) Reformed<br>`RK` = (RK) Roman Catholic |
| 78 | `RelPartner` | Religion of Partner | nVarChar | 9 | - | 0 | `0`<br>`--` = No Church Tax Liability<br>`AK` = (AK) Old Catholic<br>`EV` = (EV) Protestant<br>`FA` = (FA) Non-Denomination Alzey<br>`FB` = (FB) Non-Denominational Regional Congregation Baden<br>`FG` = (FG) Non-Denominational Regional Congregation Palatinate<br>`FM` = (FM) Non-Denominational Congregation Mainz<br>`FR` = (FR) French-Reformed<br>`FS` = (FS) Non-Denominational Congregation Offenbach/Mainz<br>`IB` = (IB) Israelite Religious Community Baden<br>`IL` = (IL) Israelite Rural<br>`IS` = (IS) Israelite<br>`IW` = (IW) Israelite Religious Community Wuerttemberg<br>`JD` = (JD) Jewish Religion Tax<br>`JH` = (JH) Jewish Religion Tax<br>`JS` = (JS) Jewish Religion Tax<br>`LT` = (LT) Lutheran<br>`RF` = (RF) Reformed<br>`RK` = (RK) Roman Catholic |
| 79 | `ExemptAmnt` | Exemption Amount | Num | 19.6 | - |  |  |
| 80 | `ExemptUnit` | Exemption Amount Period | nVarChar | 20 | - | 0 | `0`<br>`1` = Yearly<br>`2` = Monthly<br>`3` = Weekly<br>`4` = Daily |
| 81 | `AddiAmnt` | Additional Amount | Num | 19.6 | - |  |  |
| 82 | `AddiUnit` | Additional Amount Period | nVarChar | 20 | - | 0 | `0`<br>`1` = Yearly<br>`2` = Monthly<br>`3` = Weekly<br>`4` = Daily |
| 83 | `TaxOName` | Tax Office Name | nVarChar | 50 | - |  |  |
| 84 | `TaxONum` | Tax Office Number | nVarChar | 20 | - |  |  |
| 85 | `HeaInsName` | Health Insurance Company Name | nVarChar | 50 | - |  |  |
| 86 | `HeaInsCode` | Health Insurance Code | nVarChar | 50 | - |  |  |
| 87 | `HeaInsType` | Type of Health Insurance | nVarChar | 20 | - | ' ' | `' '`<br>`AOK` = (AOK)<br>`IKK` = (IKK)<br>`EKK` = (EKK)<br>`BKK` = (BKK)<br>`BKS` = (BKS)<br>`LKK` = (LKK) |
| 88 | `SInsurNum` | Social Insurance Number | nVarChar | 20 | - |  |  |
| 89 | `StatusOfP` | Professional Status | nVarChar | 2 | - | -1 | `-1`<br>`0` = Trainee<br>`1` = Worker<br>`2` = Skilled Worker<br>`3` = Supervisor/Foreman<br>`4` = Office Worker<br>`5` = Youth Help/Sheltered Workshop<br>`6` = On Career Advancement Training<br>`7` = Homeworker<br>`8` = Part Time <18 hrs<br>`9` = Part Time > 18 Hrs |
| 90 | `StatusOfE` | Educational Status | nVarChar | 2 | - | 0 | `0`<br>`1` = W/o Professional Qualification<br>`2` = W. Professional Qualification<br>`3` = High School w/o Prof. Qualif.<br>`4` = High School w. Prof. Qualific.<br>`5` = Vocational Qualification<br>`6` = University<br>`7` = Not Possible to Specify |
| 91 | `BCodeDateV` | Bank Code for DATEV | nVarChar | 20 | - |  |  |
| 92 | `DevBAOwner` | Deviating Bank Account Owner | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 93 | `FNameSP` | First Name of Spouse | nVarChar | 50 | - |  |  |
| 94 | `SurnameSP` | Last Name of Spouse | nVarChar | 50 | - |  |  |
| 95 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 96 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 97 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 98 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 99 | `PersGroup` | Person Group | nVarChar | 5 | - | -1 | `-1`<br>`101` = Subject to Social Insurance<br>`102` = Apprentice<br>`104` = Home Worker<br>`105` = Trainee<br>`106` = Student<br>`108` = Early Retirement<br>`109` = Part-Time Employee<br>`110` = Short-Term Employee<br>`112` = Family Member: Agriculture<br>`113` = Addnl Income: Agriculture<br>`114` = Addnl Income: Seasonal Agriculture<br>`116` = Receiving Compensation Pay<br>`118` = Irregularly Employed<br>`119` = Pensioner<br>`997` = Not Specified |
| 100 | `JTCode` | Job Title Code | nVarChar | 5 | - |  |  |
| 101 | `ExtEmpNo` | Ext. Employee No. | nVarChar | 20 | - |  |  |
| 102 | `BirthPlace` | Place of Birth | nVarChar | 100 | - |  |  |
| 103 | `PymMeth` | Payment Method | nVarChar | 2 | - | 05 | `-1`<br>`05` = Bank Transfer |
| 104 | `ExemptCurr` | Exemption Amount Currency | nVarChar | 3 | - |  |  |
| 105 | `AddiCurr` | Additional Amount Currency | nVarChar | 3 | - |  |  |
| 106 | `STDCode` | STD Code | Int | 11 | - |  |  |
| 107 | `FatherName` | Father's Name | nVarChar | 150 | - |  |  |
| 108 | `CPF` | Personal Fiscal ID | nVarChar | 100 | - |  |  |
| 109 | `CRC` | CRC Number | nVarChar | 20 | - |  |  |
| 110 | `ContResp` | Accountant Responsible | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 111 | `RepLegal` | Legal Representative | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 112 | `DirfDeclar` | DIRF Responsible | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 113 | `UF_CRC` | CRC State | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 114 | `IDType` | ID Type | nVarChar | 30 | [OIDT](OIDT.md) |  |  |
| 115 | `Active` | Employee Status | VarChar | 1 | - | Y | `Y` = Active<br>`N` = Inactive |
| 116 | `BPLId` | Branch | Int | 11 | [OBPL](OBPL.md) |  |  |
| 117 | `ManualNUM` | Manual EMP No. | nVarChar | 60 | - |  |  |
| 118 | `PassIssue` | Passport Issue Date | Date | 8 | - |  |  |
| 119 | `PassIssuer` | Passport Issuer | nVarChar | 254 | - |  |  |
| 120 | `QualCode` | Qualification Code | nVarChar | 3 | - | 000 | `000` = n/a<br>`203` = Diretor<br>`204` = Conselheiro de Administra��o<br>`205` = Administrador<br>`206` = Administrador do Grupo<br>`207` = Administrador de Sociedade Filiada<br>`220` = Administrador Judicial - Pessoa Fisica<br>`222` = Administrador Judicial - Pessoa Juridica - profissional respons�vel<br>`223` = Administrador Judicial / Gestor<br>`226` = Gestor Judicial<br>`309` = Procurador<br>`312` = Inventariante<br>`313` = Liquidante<br>`315` = Interventor<br>`801` = Empres�rio<br>`900` = Contador<br>`999` = Outros |
| 121 | `PRWebAccss` | Enable Access to PR from Web | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 122 | `PrePRWeb` | Previous Stats of PR Web Access | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 123 | `BPLink` | BP Link | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 124 | `NaturalPer` | Natural Person | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 125 | `DPPStatus` | Data Protection Status | VarChar | 1 | - | N | `N` = None<br>`D` = Erased<br>`B` = Blocked<br>`U` = Unblocked |
| 126 | `EnRligion` | Encryption of Religion | Text | 16 | - |  |  |
| 127 | `EnRligionP` | Encryption of Religion Partner | Text | 16 | - |  |  |
| 128 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 129 | `EnGovID` | Encryption of Government ID | Text | 16 | - |  |  |
| 130 | `EnPassport` | Encryption of Passport No. | Text | 16 | - |  |  |
| 131 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 132 | `CreateTS` | Creation Time Incl. Sec. | Int | 11 | - |  |  |
| 133 | `UpdateTS` | Update Full Time | Int | 11 | - |  |  |
| 134 | `EnInsurNum` | Encryption of Social Insurance No. | Text | 16 | - |  |  |
| 135 | `EnBnkAcct` | Encryption of Bank Account | Text | 16 | - |  |  |
| 136 | `Code` | Employee Code | nVarChar | 50 | - |  |  |
| 137 | `ARetSEFAZ` | Authorization to Retrieve NFe from SEFAZ | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 138 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer<br>`G` = Fixed Assets Migration |
| 139 | `EnSex` | Encryption of Sex | Text | 16 | - |  |  |
| 140 | `SexEx` | Gender | nVarChar | 15 | [OGDR](OGDR.md) | M |  |
| 141 | `EnSexEx` | Encryption of SexEx | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | empID, LogInstanc |
