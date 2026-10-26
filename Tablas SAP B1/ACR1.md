# ACR1 - Business Partner Addresses - History

- **Tabla:** ACR1
- **Descripción:** Business Partner Addresses - History
- **Cantidad de campos:** 45
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ACR1.html

## Campos (45)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Address` | Address Name | nVarChar | 50 | - |  |  |
| 2 | `CardCode` | BP Code | nVarChar | 15 | [ACRD](ACRD.md) |  |  |
| 3 | `Street` | Street | nVarChar | 100 | - |  |  |
| 4 | `Block` | Block | nVarChar | 100 | - |  |  |
| 5 | `ZipCode` | Zip Code | nVarChar | 20 | - |  |  |
| 6 | `City` | City | nVarChar | 100 | - |  |  |
| 7 | `County` | County | nVarChar | 100 | - |  |  |
| 8 | `Country` | Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 9 | `State` | State | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 10 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 11 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 12 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 2 |  |
| 13 | `LicTradNum` | Federal Tax ID | nVarChar | 32 | - |  |  |
| 14 | `LineNum` | Row No. | Int | 11 | - |  |  |
| 15 | `TaxCode` | Tax Code | nVarChar | 8 | [OSTC](OSTC.md) |  |  |
| 16 | `Building` | Building/Floor/Room | Text | 16 | - |  |  |
| 17 | `AdresType` | Address Type | VarChar | 1 | - | S | `S` = Ship To<br>`B` = Bill To |
| 18 | `Address2` | Address Name 2 | nVarChar | 50 | - |  |  |
| 19 | `Address3` | Address Name 3 | nVarChar | 50 | - |  |  |
| 20 | `AddrType` | Address Type | nVarChar | 100 | - |  |  |
| 21 | `StreetNo` | Street No. | nVarChar | 100 | - |  |  |
| 22 | `AltCrdName` | Alternative BP Name | nVarChar | 200 | - |  |  |
| 23 | `AltTaxId` | Alternative Tax ID | nVarChar | 32 | - |  |  |
| 24 | `TaxOffice` | Tax Office | nVarChar | 50 | - |  |  |
| 25 | `GlblLocNum` | Global Location Number | nVarChar | 50 | - |  |  |
| 26 | `Ntnlty` | Nationality | nVarChar | 100 | - |  |  |
| 27 | `DIOTNat` | DIOT Nationality | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 28 | `TaaSEnbl` | TaaS Service Enabled on Address | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 29 | `GSTRegnNo` | GSTIN | nVarChar | 15 | - |  |  |
| 30 | `GSTType` | GST Type | Int | 11 | [OGTY](OGTY.md) |  |  |
| 31 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 32 | `CreateTS` | Creation Time Incl. Sec. | Int | 11 | - |  |  |
| 33 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 34 | `MYFType` | MYF Type | nVarChar | 2 | - |  | `S1` = MYF Wholesale Sales<br>`S2` = Retail Sales<br>`P1` = MYF Wholesale Purchases<br>`P3` = Other Expense Transactions |
| 35 | `VatResDate` | VAT Verfication Response Date | Date | 8 | - |  |  |
| 36 | `VatResCode` | VAT Verfication Response Code | Int | 11 | [ORVC](ORVC.md) |  |  |
| 37 | `VatResName` | VAT Verfication Response Name | nVarChar | 254 | - |  |  |
| 38 | `VatResAddr` | VAT Verfication Response Addr | nVarChar | 254 | - |  |  |
| 39 | `EnNtnlty` | Encryption of Nationality | Text | 16 | - |  |  |
| 40 | `EnLicTradN` | Encrypt TAX ID Number | Text | 16 | - |  |  |
| 41 | `Active` | Active | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 42 | `AlwChInAdd` | Allow Changes in Address Components | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 43 | `SiretNo` | SIRET No. | nVarChar | 32 | - |  |  |
| 44 | `RoutingCod` | Routing Code | nVarChar | 100 | - |  |  |
| 45 | `Suffix` | Suffix | nVarChar | 20 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CardCode, Address, AdresType, LogInstanc |
