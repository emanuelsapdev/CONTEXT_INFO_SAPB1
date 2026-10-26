# SCL6 - Service Call Scheduling

- **Tabla:** SCL6
- **Descripción:** Service Call Scheduling
- **Cantidad de campos:** 52
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SCL6.html

## Campos (52)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `SrcvCallID` | Service Call No. | Int | 11 | [OSCL](OSCL.md) |  |  |
| 2 | `Line` | Row | Int | 6 | - |  |  |
| 3 | `Technician` | Technician | Int | 11 | [OHEM](OHEM.md) |  |  |
| 4 | `HandledBy` | Handled by User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 5 | `StartDate` | Start Date | Date | 8 | - |  |  |
| 6 | `StartTime` | Start Time | Int | 11 | - |  |  |
| 7 | `EndDate` | End Date | Date | 8 | - |  |  |
| 8 | `EndTime` | End Time | Int | 11 | - |  |  |
| 9 | `Duration` | Service Call Duration | Num | 19.6 | - |  |  |
| 10 | `Location` | Location | Int | 6 | [OCLO](OCLO.md) | -1 |  |
| 11 | `AddressId` | Address Code | nVarChar | 50 | - |  |  |
| 12 | `Address` | Address | nVarChar | 254 | - |  |  |
| 13 | `Reminder` | Reminder | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 14 | `RemQty` | Reminder Quantity | Num | 19.6 | - |  |  |
| 15 | `DisplInCal` | Display in Calendar | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 16 | `Unsched` | Unscheduled Call | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 17 | `DurType` | Duration UoM | VarChar | 1 | - | M | `S` = Seconds<br>`M` = Minutes<br>`H` = Hours<br>`D` = Days |
| 18 | `RemType` | Reminder UoM | VarChar | 1 | - | M | `S` = Seconds<br>`M` = Minutes<br>`H` = Hours<br>`D` = Days |
| 19 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 20 | `RemDate` | Reminder Date | Date | 8 | - |  |  |
| 21 | `RemSent` | Reminder Sent | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 22 | `RemTime` | Reminder Time | Int | 6 | - |  |  |
| 23 | `Street` | Street | nVarChar | 100 | - |  |  |
| 24 | `City` | City | nVarChar | 100 | - |  |  |
| 25 | `Room` | Room | nVarChar | 50 | - |  |  |
| 26 | `State` | State | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 27 | `Country` | Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 28 | `Address2` | Address Name 2 | nVarChar | 50 | - |  |  |
| 29 | `Address3` | Address Name 3 | nVarChar | 50 | - |  |  |
| 30 | `AddrType` | Address Type | nVarChar | 100 | - |  |  |
| 31 | `StreetNo` | Street No. | nVarChar | 100 | - |  |  |
| 32 | `ZipCode` | Zip Code | nVarChar | 20 | - |  |  |
| 33 | `Block` | Block | nVarChar | 100 | - |  |  |
| 34 | `County` | County | nVarChar | 100 | - |  |  |
| 35 | `TaxOffice` | Tax Office | nVarChar | 50 | - |  |  |
| 36 | `GlblLocNum` | Global Location Number | nVarChar | 50 | - |  |  |
| 37 | `ActualDur` | Actual Duration | Num | 19.6 | - |  |  |
| 38 | `ActDurType` | Actual Duration UoM | VarChar | 1 | - | M | `S` = Seconds<br>`M` = Minutes<br>`H` = Hours<br>`D` = Days |
| 39 | `Close` | Close | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 40 | `Remark` | Remarks | nVarChar | 254 | - |  |  |
| 41 | `AddrTypeBS` | Address Type | VarChar | 1 | - |  | `S` = Ship To<br>`B` = Bill To |
| 42 | `SignName` | Signature Name | nVarChar | 100 | - |  |  |
| 43 | `SaleOrders` | Sales Orders | nVarChar | 100 | - |  |  |
| 44 | `ChkInDate` | Check in Date | Date | 8 | - |  |  |
| 45 | `ChkInTime` | Check in Time | Int | 11 | - |  |  |
| 46 | `ChkInLoc` | Check in Location | nVarChar | 254 | - |  |  |
| 47 | `ChkLontitu` | Check in Longitude | nVarChar | 14 | - |  |  |
| 48 | `ChkLatitu` | Check in Latitude | nVarChar | 13 | - |  |  |
| 49 | `ChkOutDate` | Check out Date | Date | 8 | - |  |  |
| 50 | `ChkOutTime` | Check out Time | Int | 11 | - |  |  |
| 51 | `SignData` | Signature Data | Text | 16 | - |  |  |
| 52 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | SrcvCallID, Line |
