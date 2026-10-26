# ASC7 - Service Call BP Address

- **Tabla:** ASC7
- **Descripción:** Service Call BP Address
- **Cantidad de campos:** 67
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ASC7.html

## Campos (67)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | [OSCL](OSCL.md) |  |  |
| 2 | `TaxId0` | Tax ID 0 | nVarChar | 100 | - |  |  |
| 3 | `TaxId1` | Tax ID 1 | nVarChar | 100 | - |  |  |
| 4 | `TaxId2` | Tax ID 2 | nVarChar | 100 | - |  |  |
| 5 | `TaxId3` | Tax ID 3 | nVarChar | 100 | - |  |  |
| 6 | `TaxId4` | Tax ID 4 | nVarChar | 100 | - |  |  |
| 7 | `TaxId5` | Tax ID 5 | nVarChar | 100 | - |  |  |
| 8 | `TaxId6` | Tax ID 6 | nVarChar | 100 | - |  |  |
| 9 | `TaxId7` | Tax ID 7 | nVarChar | 100 | - |  |  |
| 10 | `TaxId8` | Tax ID 8 | nVarChar | 100 | - |  |  |
| 11 | `TaxId9` | Tax ID 9 | nVarChar | 100 | - |  |  |
| 12 | `State` | State Code | nVarChar | 3 | - |  |  |
| 13 | `County` | County Code | nVarChar | 7 | - |  |  |
| 14 | `Incoterms` | Incoterms | nVarChar | 3 | - |  |  |
| 15 | `Vehicle` | Vehicle ID | nVarChar | 10 | - |  |  |
| 16 | `VidState` | Vehicle ID (State) | nVarChar | 3 | - |  |  |
| 17 | `NfRef` | NF Reference | nVarChar | 254 | - |  |  |
| 18 | `Carrier` | Carrier Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 19 | `QoP` | Quantity of Packs | Int | 11 | - |  |  |
| 20 | `PackDesc` | Pack Description | nVarChar | 10 | - |  |  |
| 21 | `Brand` | Brand | nVarChar | 20 | - |  |  |
| 22 | `NoSU` | Number of Shipping Unit | Int | 11 | - |  |  |
| 23 | `NetWeight` | Net Weight | Num | 19.6 | - |  |  |
| 24 | `GrsWeight` | Gross Weight | Num | 19.6 | - |  |  |
| 25 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 26 | `ObjectType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 191 |  |
| 27 | `TaxId10` | Tax ID 10 | nVarChar | 100 | - |  |  |
| 28 | `TransCat` | Transaction Category | nVarChar | 100 | - |  |  |
| 29 | `FormNo` | Form No. | nVarChar | 100 | - |  |  |
| 30 | `TaxId11` | Tax ID 11 | nVarChar | 100 | - |  |  |
| 31 | `StreetS` | Street | nVarChar | 100 | - |  |  |
| 32 | `BlockS` | Block | nVarChar | 100 | - |  |  |
| 33 | `BuildingS` | Building/Floor/Room | Text | 16 | - |  |  |
| 34 | `CityS` | City | nVarChar | 100 | - |  |  |
| 35 | `ZipCodeS` | Zip Code | nVarChar | 20 | - |  |  |
| 36 | `CountyS` | County | nVarChar | 100 | - |  |  |
| 37 | `StateS` | State | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 38 | `CountryS` | Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 39 | `AddrTypeS` | Address Type | nVarChar | 100 | - |  |  |
| 40 | `StreetNoS` | Street No. | nVarChar | 100 | - |  |  |
| 41 | `StreetB` | Street | nVarChar | 100 | - |  |  |
| 42 | `BlockB` | Block | nVarChar | 100 | - |  |  |
| 43 | `BuildingB` | Building/Floor/Room | Text | 16 | - |  |  |
| 44 | `CityB` | City | nVarChar | 100 | - |  |  |
| 45 | `ZipCodeB` | Zip Code | nVarChar | 20 | - |  |  |
| 46 | `CountyB` | County | nVarChar | 100 | - |  |  |
| 47 | `StateB` | State | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 48 | `CountryB` | Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 49 | `AddrTypeB` | Address Type | nVarChar | 100 | - |  |  |
| 50 | `StreetNoB` | Street No. | nVarChar | 100 | - |  |  |
| 51 | `ImpORExp` | Import or Export | VarChar | 1 | - |  | `N`<br>`Y` |
| 52 | `Vat` | VAT | VarChar | 1 | - | N | `N` = No VAT Support<br>`Y` = VAT Support |
| 53 | `AltCrdNamB` | Alternative BP Name | nVarChar | 200 | - |  |  |
| 54 | `AltTaxIdB` | Alternative Tax ID | nVarChar | 32 | - |  |  |
| 55 | `Address2S` | Address Name 2 | nVarChar | 50 | - |  |  |
| 56 | `Address3S` | Address Name 3 | nVarChar | 50 | - |  |  |
| 57 | `Address2B` | Address Name 2 | nVarChar | 50 | - |  |  |
| 58 | `Address3B` | Address Name 3 | nVarChar | 50 | - |  |  |
| 59 | `MainUsage` | Main Usage Code of Document | Int | 11 | [OUSG](OUSG.md) |  |  |
| 60 | `GlbLocNumS` | Global Location Number | nVarChar | 50 | - |  |  |
| 61 | `GlbLocNumB` | Global Location Number | nVarChar | 50 | - |  |  |
| 62 | `CollectDT` | Date and Time of Collection | nVarChar | 20 | - |  |  |
| 63 | `TransprtDT` | Transport Starting Date | Date | 8 | - |  |  |
| 64 | `TransprtRS` | Transport Reason | nVarChar | 100 | - |  |  |
| 65 | `TaxId12` | Tax ID 12 | nVarChar | 50 | - |  |  |
| 66 | `TaxId13` | Deductee Ref. No. in India | nVarChar | 100 | - |  |  |
| 67 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LogInstanc |
