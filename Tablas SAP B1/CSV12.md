# CSV12 - A/R Correction Invoice Reversal - Tax Extension

- **Tabla:** CSV12
- **Descripción:** A/R Correction Invoice Reversal - Tax Extension
- **Cantidad de campos:** 130
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CSV12.html

## Campos (130)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | [OCSV](OCSV.md) |  |  |
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
| 18 | `Carrier` | Carrier Code | nVarChar | 15 | - |  |  |
| 19 | `QoP` | Quantity of Packs | Int | 11 | - |  |  |
| 20 | `PackDesc` | Pack Description | nVarChar | 10 | - |  |  |
| 21 | `Brand` | Brand | nVarChar | 20 | - |  |  |
| 22 | `NoSU` | Number of Shipping Unit | Int | 11 | - |  |  |
| 23 | `NetWeight` | Net Weight | Num | 19.6 | - |  |  |
| 24 | `GrsWeight` | Gross Weight | Num | 19.6 | - |  |  |
| 25 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 26 | `ObjectType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 166 |  |
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
| 67 | `ImpExpNo` | Import/Export Bill No. | nVarChar | 100 | - |  |  |
| 68 | `ImpExpDate` | Import/Export Date | Date | 8 | - |  |  |
| 69 | `BpGSTType` | GST Regn Type of BP | Int | 11 | - |  |  |
| 70 | `BpGSTN` | GST Regn No of BP | nVarChar | 15 | - |  |  |
| 71 | `BpStateCod` | State Code of Business Partner | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 72 | `BPStatGSTN` | GST State Code of BP | nVarChar | 2 | - |  |  |
| 73 | `LocGSTType` | GST Regn Type of Location | Int | 11 | - |  |  |
| 74 | `LocGSTN` | GST Regn No of Location | nVarChar | 15 | - |  |  |
| 75 | `LocStatCod` | State Code of Location | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 76 | `LocStaGSTN` | GST State Code of Location | nVarChar | 2 | - |  |  |
| 77 | `BpCountry` | Country/Region Code of BP | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 78 | `OrigImpNo` | Original Bill of Entry No. | nVarChar | 100 | - |  |  |
| 79 | `OrigImpDat` | Original Bill of Entry Date | Date | 8 | - |  |  |
| 80 | `ExportType` | Exporting Type | VarChar | 1 | - | E | `E` = Imports/Exports<br>`S` = SEZ Developer<br>`U` = SEZ Unit<br>`D` = Deemed Imports/Exports |
| 81 | `PortCode` | Port Code | nVarChar | 100 | - |  |  |
| 82 | `BoEValue` | Bill of Entry Value | Num | 19.6 | - |  |  |
| 83 | `IsIGSTAct` | Supply under IGST Account | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 84 | `ClaimRefun` | Claim Refund | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 85 | `TaxRateDif` | Differential % of Tax Rate | Int | 11 | - |  | `65`<br>`100` |
| 86 | `BPGdsIssP` | Goods Issue Place BP | nVarChar | 15 | - |  |  |
| 87 | `CNPJGIP` | Goods Issue Place CNPJ | nVarChar | 100 | - |  |  |
| 88 | `CPFGIP` | Goods Issue Place CPF | nVarChar | 100 | - |  |  |
| 89 | `StreetGIP` | Goods Issue Place Street | nVarChar | 100 | - |  |  |
| 90 | `StrtNoGIP` | Goods Issue Place Street No. | nVarChar | 100 | - |  |  |
| 91 | `BldngGIP` | Goods Issue Place Building | Text | 16 | - |  |  |
| 92 | `ZipGIP` | Goods Issue Place Zip Code | nVarChar | 20 | - |  |  |
| 93 | `BlockGIP` | Goods Issue Place Block | nVarChar | 100 | - |  |  |
| 94 | `CityGIP` | Goods Issue Place City | nVarChar | 100 | - |  |  |
| 95 | `CountyGIP` | Goods Issue Place County | nVarChar | 100 | - |  |  |
| 96 | `StateGIP` | Goods Issue Place State | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 97 | `CountryGIP` | Goods Issue Place Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 98 | `PhoneGIP` | Goods Issue Place Phone | nVarChar | 20 | - |  |  |
| 99 | `EMailGIP` | Goods Issue Place E-Mail | nVarChar | 100 | - |  |  |
| 100 | `DptDateGIP` | Goods Issue Place Departure Date | Date | 8 | - |  |  |
| 101 | `BPDelivryP` | Delivery Place BP | nVarChar | 15 | - |  |  |
| 102 | `CNPJDlvryP` | Delivery Place CNPJ | nVarChar | 100 | - |  |  |
| 103 | `CPFDlvryP` | Delivery Place CPF | nVarChar | 100 | - |  |  |
| 104 | `StrtDlvryP` | Delivery Place Street | nVarChar | 100 | - |  |  |
| 105 | `StrNoDlvrP` | Delivery Place Street No. | nVarChar | 100 | - |  |  |
| 106 | `BldDlvryP` | Delivery Place Building | Text | 16 | - |  |  |
| 107 | `ZipDlvryP` | Delivery Place Zip Code | nVarChar | 20 | - |  |  |
| 108 | `BlckDlvryP` | Delivery Place Block | nVarChar | 100 | - |  |  |
| 109 | `CityDlvryP` | Delivery Place City | nVarChar | 100 | - |  |  |
| 110 | `CntyDlvryP` | Delivery Place County | nVarChar | 100 | - |  |  |
| 111 | `StatDlvryP` | Delivery Place State | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 112 | `CtryDlvryP` | Delivery Place Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 113 | `FoneDlvryP` | Delivery Place Phone | nVarChar | 20 | - |  |  |
| 114 | `MailDlvryP` | Delivery Place E-Mail | nVarChar | 100 | - |  |  |
| 115 | `DpDtDlvryP` | Delivery Place Departure Date | Date | 8 | - |  |  |
| 116 | `AuthedCNPJ` | Authorized CNPJ or CPF | nVarChar | 250 | - |  |  |
| 117 | `TaxId14` | ITR Filing | nVarChar | 250 | - |  |  |
| 118 | `StreetR` | Street for Return | nVarChar | 100 | - |  |  |
| 119 | `BlockR` | Block for Return | nVarChar | 100 | - |  |  |
| 120 | `BuildingR` | Building / Floor / Room for Return | Text | 16 | - |  |  |
| 121 | `CityR` | City for Return | nVarChar | 100 | - |  |  |
| 122 | `ZipCodeR` | Zip Code for Return | nVarChar | 20 | - |  |  |
| 123 | `CountyR` | County for Return | nVarChar | 100 | - |  |  |
| 124 | `StateR` | State for Return | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 125 | `CountryR` | Country/Region for Return | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 126 | `AddrTypeR` | Address Type for Return | nVarChar | 100 | - |  |  |
| 127 | `StreetNoR` | Street No. for Return | nVarChar | 100 | - |  |  |
| 128 | `Address2R` | Address Name 2 for Return | nVarChar | 50 | - |  |  |
| 129 | `Address3R` | Address Name 3 for Return | nVarChar | 50 | - |  |  |
| 130 | `GlbLocNumR` | Global Location Number for Return | nVarChar | 50 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry |
