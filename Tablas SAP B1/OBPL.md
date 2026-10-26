# OBPL - Branches

- **Tabla:** OBPL
- **Descripción:** Branches
- **Cantidad de campos:** 56
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OBPL.html

## Campos (56)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `BPLId` | Branch ID | Int | 11 | - |  |  |
| 2 | `BPLName` | Branch Name | nVarChar | 200 | - |  |  |
| 3 | `BPLFrName` | Branch Name (Foreign) | nVarChar | 200 | - |  |  |
| 4 | `VATRegNum` | VAT Reg. Number | nVarChar | 12 | - |  |  |
| 5 | `RepName` | Rep. Name | nVarChar | 15 | - |  |  |
| 6 | `Industry` | Industry | nVarChar | 20 | - |  |  |
| 7 | `Business` | Business | nVarChar | 20 | - |  |  |
| 8 | `Address` | Address | nVarChar | 254 | - |  |  |
| 9 | `AddressFr` | Address (Foreign) | nVarChar | 254 | - |  |  |
| 10 | `MainBPL` | Main BPL | VarChar | 1 | - | N | `Y` = Main Business Place<br>`N` = Not Main Business Place |
| 11 | `TxOffcNo` | Tax Office No. | nVarChar | 3 | - |  |  |
| 12 | `Disabled` | Disabled | VarChar | 1 | - | N | `Y` = Disabled<br>`N` = Enabled |
| 13 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 14 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 15 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 16 | `DflCust` | Default Customer ID | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 17 | `DflVendor` | Default Vendor ID | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 18 | `DflWhs` | Default Warehouse ID | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 19 | `DflTaxCode` | Default Tax Code | nVarChar | 8 | [OCNA](OCNA.md) |  |  |
| 20 | `RevOffice` | Tax Office | nVarChar | 100 | - |  |  |
| 21 | `TaxIdNum` | Branch Reg. No. | nVarChar | 32 | - |  |  |
| 22 | `TaxIdNum2` | Federal Tax ID 2 | nVarChar | 32 | - |  |  |
| 23 | `TaxIdNum3` | Federal Tax ID 3 | nVarChar | 32 | - |  |  |
| 24 | `AddtnlId` | Additional ID Number | nVarChar | 32 | - |  |  |
| 25 | `CompNature` | Nature of Company | Int | 11 | [OBNI](OBNI.md) | -1 |  |
| 26 | `EconActT` | Economic Activity Type | Int | 11 | [OBNI](OBNI.md) | -1 |  |
| 27 | `CredCOrig` | Credit Contribution Origin | nVarChar | 2 | [OBSI](OBSI.md) |  |  |
| 28 | `IPIPeriod` | IPI Period | nVarChar | 2 | [OBSI](OBSI.md) |  |  |
| 29 | `CoopAssocT` | Cooperative Association Type | Int | 11 | [OBNI](OBNI.md) | -1 |  |
| 30 | `PrefState` | Default State | nVarChar | 3 | - |  |  |
| 31 | `ProfTax` | Profit Taxation | Int | 11 | [OBNI](OBNI.md) | -1 |  |
| 32 | `CompQualif` | Company Qualification | Int | 11 | [OBNI](OBNI.md) | -1 |  |
| 33 | `DeclType` | Declarer Type | Int | 11 | [OBNI](OBNI.md) | -1 |  |
| 34 | `AddrType` | Address Type | nVarChar | 100 | - |  |  |
| 35 | `Street` | Street | nVarChar | 100 | - |  |  |
| 36 | `StreetNo` | Street No. | nVarChar | 100 | - |  |  |
| 37 | `Building` | Building/Floor/Room | nVarChar | 100 | - |  |  |
| 38 | `ZipCode` | Zip Code | nVarChar | 20 | - |  |  |
| 39 | `Block` | Block | nVarChar | 100 | - |  |  |
| 40 | `City` | City | nVarChar | 100 | - |  |  |
| 41 | `State` | State | nVarChar | 3 | - |  |  |
| 42 | `County` | County | nVarChar | 100 | [OCNT](OCNT.md) |  |  |
| 43 | `Country` | Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 44 | `PmtClrAct` | Payment Clearing Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 45 | `CommerReg` | Commercial Register | nVarChar | 60 | - |  |  |
| 46 | `DateOfInc` | Date of Incorporation | Date | 8 | - |  |  |
| 47 | `SPEDProf` | SPED Profile | nVarChar | 2 | [OBSI](OBSI.md) |  |  |
| 48 | `EnvTypeNFe` | Environment Type NFe | Int | 11 | [OBNI](OBNI.md) | -1 |  |
| 49 | `Opt4ICMS` | Opting for ICMS 115_03 | VarChar | 1 | - | N |  |
| 50 | `AliasName` | Alias Name | Text | 16 | - |  |  |
| 51 | `GlblLocNum` | Global Location Number | nVarChar | 50 | - |  |  |
| 52 | `TaxRptFrm` | Tax Wizard Reporting From | Date | 8 | - |  |  |
| 53 | `Suframa` | SUFRAMA | nVarChar | 100 | - |  |  |
| 54 | `DfltResWhs` | Default Resource Warehouse ID | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 55 | `SnapshotId` | Snapshot ID | Int | 11 | - | 0 |  |
| 56 | `BPLNum` | Branch No. | Int | 11 | - | 0 |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | BPLId |
| NAME | Yes | BPLName |
