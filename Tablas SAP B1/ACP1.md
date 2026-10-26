# ACP1 - Campaign - BPs

- **Tabla:** ACP1
- **Descripción:** Campaign - BPs
- **Cantidad de campos:** 47
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ACP1.html

## Campos (47)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CpnNo` | Campaign No. | Int | 11 | [OCPN](OCPN.md) |  |  |
| 2 | `CpnLineNum` | Campaign Line Number | Int | 11 | - |  |  |
| 3 | `BpCode` | BP Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 4 | `BpName` | BP Name | nVarChar | 200 | - |  |  |
| 5 | `GroupName` | BP Group Name | nVarChar | 100 | - |  |  |
| 6 | `Industry` | BP Industry Name | nVarChar | 40 | - |  |  |
| 7 | `Status` | BP Status | VarChar | 1 | - |  | `A` = Active<br>`I` = Inactive |
| 8 | `CntCode` | Contact Code | nVarChar | 50 | - |  |  |
| 9 | `CntTitle` | Contact Title | nVarChar | 10 | - |  |  |
| 10 | `CntPstn` | Contact Position | nVarChar | 90 | - |  |  |
| 11 | `CntEmail` | Contact E-Mail | nVarChar | 100 | - |  |  |
| 12 | `CntTel` | Contact Telephone | nVarChar | 50 | - |  |  |
| 13 | `CntMobile` | Contact Mobile | nVarChar | 50 | - |  |  |
| 14 | `CntFax` | Contact Fax | nVarChar | 50 | - |  |  |
| 15 | `CntAddr` | Contact Address | nVarChar | 254 | - |  |  |
| 16 | `Response` | Response from Company | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 17 | `OpprId` | Related Opportunity | Int | 11 | [OOPR](OOPR.md) |  |  |
| 18 | `LogIns` | Log Instance - History | Int | 11 | - |  |  |
| 19 | `VisOrder` | Visual Order | Int | 11 | - |  |  |
| 20 | `Street` | Street | nVarChar | 100 | - |  |  |
| 21 | `Block` | Block | nVarChar | 100 | - |  |  |
| 22 | `City` | City | nVarChar | 100 | - |  |  |
| 23 | `ZipCode` | Zip Code | nVarChar | 100 | - |  |  |
| 24 | `County` | County | nVarChar | 100 | - |  |  |
| 25 | `State` | State | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 26 | `Country` | Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 27 | `Building` | Building/Floor/Room | Text | 16 | - |  |  |
| 28 | `CActivity` | Create Activity [Y/N] | VarChar | 1 | - | Y |  |
| 29 | `DocType` | Document Type | nVarChar | 20 | - | -1 | `E`<br>`P` = Opportunities<br>`Q` = Sales Quotations<br>`O` = Sales Orders<br>`D` = Deliveries<br>`I` = A/R Invoices<br>`-97` = Purchase Opportunities<br>`540000006` = Purchase Quotations<br>`22` = Purchase Orders<br>`20` = Goods Receipt POs<br>`18` = A/P Invoices |
| 30 | `ShowBPDoc` | Show BP Documents [Y/N] | VarChar | 1 | - | N |  |
| 31 | `DocNumber` | Related Document | Int | 11 | - |  |  |
| 32 | `DocEntry` | Document Entry | Int | 11 | - |  |  |
| 33 | `AssignTo` | Assign to User or Employee | VarChar | 1 | - | U | `U` = User<br>`E` = Employee |
| 34 | `AssignName` | User or Employee Name | Int | 11 | - |  |  |
| 35 | `FirstName` | First Name | nVarChar | 50 | - |  |  |
| 36 | `MiddleName` | Middle Name | nVarChar | 50 | - |  |  |
| 37 | `LastName` | Last Name | nVarChar | 50 | - |  |  |
| 38 | `LicTradNum` | Federal Tax ID | nVarChar | 32 | - |  |  |
| 39 | `AddrType` | Address Type | nVarChar | 100 | - |  |  |
| 40 | `Address2` | Address Name 2 | nVarChar | 50 | - |  |  |
| 41 | `Address3` | Address Name 3 | nVarChar | 50 | - |  |  |
| 42 | `StreetNo` | Street No. | nVarChar | 100 | - |  |  |
| 43 | `AddressID` | Address ID | nVarChar | 50 | - |  |  |
| 44 | `RspType` | Response Type | nVarChar | 20 | [ORPT](ORPT.md) |  |  |
| 45 | `DPPStatus` | Data Protection Status | VarChar | 1 | - | N | `N` = None<br>`D` = Erased<br>`B` = Blocked<br>`U` = Unblocked |
| 46 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 47 | `EnLicTradN` | Encrypt TAX ID Number | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CpnNo, CpnLineNum, LogIns |
