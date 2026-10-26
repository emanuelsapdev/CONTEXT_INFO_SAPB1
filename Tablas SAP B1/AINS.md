# AINS - Customer Equipment Card - History

- **Tabla:** AINS
- **Descripción:** Customer Equipment Card - History
- **Cantidad de campos:** 56
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AINS.html

## Campos (56)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `insID` | Equipment Card Number | Int | 11 | - |  |  |
| 2 | `customer` | Business Partner Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 3 | `custmrName` | Business Partner Name | nVarChar | 200 | - |  |  |
| 4 | `contactCod` | Contact Person Code | Int | 11 | [OCPR](OCPR.md) |  |  |
| 5 | `directCsmr` | Direct Customer | nVarChar | 15 | - |  |  |
| 6 | `drctCsmNam` | Direct Customer Name | nVarChar | 200 | - |  |  |
| 7 | `manufSN` | Mfr. Serial No. | nVarChar | 36 | - |  |  |
| 8 | `internalSN` | Serial Number | nVarChar | 36 | - |  |  |
| 9 | `warranty` | Warranty Flag | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 10 | `wrrntyStrt` | Warranty Start Date | Date | 8 | - |  |  |
| 11 | `wrrntyEnd` | Warranty End Date | Date | 8 | - |  |  |
| 12 | `responsVal` | Time Required for Response | Int | 6 | - |  |  |
| 13 | `responsUnt` | Unit for the previous field | VarChar | 1 | - | D | `H` = Hour(s)<br>`D` = Day(s) |
| 14 | `itemCode` | Foreign Key To Item | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 15 | `itemName` | Item Description | nVarChar | 200 | - |  |  |
| 16 | `itemGroup` | Item Group | Int | 6 | [OITB](OITB.md) |  |  |
| 17 | `manufDate` | Manufacture Date | Date | 8 | - |  |  |
| 18 | `delivery` | Delivery Key | Int | 11 | [ODLN](ODLN.md) |  |  |
| 19 | `deliveryNo` | Delivery Number | Int | 11 | - |  |  |
| 20 | `invoice` | Invoice Key | Int | 11 | [OINV](OINV.md) |  |  |
| 21 | `invoiceNum` | Invoice Number | Int | 11 | - |  |  |
| 22 | `dlvryDate` | Delivery Date | Date | 8 | - |  |  |
| 23 | `cntctPhone` | Contact Phone | nVarChar | 20 | - |  |  |
| 24 | `street` | Street | nVarChar | 100 | - |  |  |
| 25 | `block` | Block | nVarChar | 100 | - |  |  |
| 26 | `zip` | Zip Code | nVarChar | 20 | - |  |  |
| 27 | `city` | City | nVarChar | 100 | - |  |  |
| 28 | `county` | County | nVarChar | 100 | - |  |  |
| 29 | `country` | Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 30 | `state` | State | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 31 | `instLction` | Installation Location | nVarChar | 254 | - |  |  |
| 32 | `contract` | Contract | Int | 11 | [OCTR](OCTR.md) |  |  |
| 33 | `cntrctStrt` | Contract Start Date | Date | 8 | - |  |  |
| 34 | `cntrctEnd` | Contract End Date | Date | 8 | - |  |  |
| 35 | `attachment` | Attachments | Text | 16 | - |  |  |
| 36 | `objType` | Object Type | nVarChar | 20 | - | 176 |  |
| 37 | `logInstanc` | Log Instance | Int | 11 | - |  |  |
| 38 | `userSign` | Creating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 39 | `createDate` | Creation Date | Date | 8 | - |  |  |
| 40 | `userSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 41 | `updateDate` | Update Date | Date | 8 | - |  |  |
| 42 | `Building` | Building/Floor/Room | Text | 16 | - |  |  |
| 43 | `status` | Status | VarChar | 1 | - | A | `A` = Active<br>`R` = Returned<br>`T` = Terminated<br>`L` = Loaned<br>`I` = In Repair Lab |
| 44 | `replcIns` | The CEC this replaced | Int | 11 | [OINS](OINS.md) |  |  |
| 45 | `repByIns` | The CEC this is replaced by | Int | 11 | [OINS](OINS.md) |  |  |
| 46 | `technician` | Default Technician | Int | 11 | [OHEM](OHEM.md) |  |  |
| 47 | `territory` | Default Territory | Int | 11 | [OTER](OTER.md) |  |  |
| 48 | `AtcEntry` | Attachment Entry | Int | 11 | [OATC](OATC.md) |  |  |
| 49 | `Transfered` | Year Transfer | VarChar | 1 | - | N |  |
| 50 | `AddrType` | Address Type | nVarChar | 100 | - |  |  |
| 51 | `Instance` | Instance | Int | 6 | - | 0 |  |
| 52 | `StreetNo` | Street No. | nVarChar | 100 | - |  |  |
| 53 | `BPType` | BP Type | VarChar | 1 | - | R | `R` = Sales<br>`P` = Purchasing<br>`B` = Sales & Purchasing |
| 54 | `OwnerCode` | Equipment Card Owner | Int | 11 | [OHEM](OHEM.md) |  |  |
| 55 | `DPPStatus` | Data Protection Status | VarChar | 1 | - | N | `N` = None<br>`D` = Erased |
| 56 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | insID, logInstanc |
