# TGG1 - Target Group Details

- **Tabla:** TGG1
- **Descripción:** Target Group Details
- **Cantidad de campos:** 32
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TGG1.html

## Campos (32)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TargetCode` | Target Group Code | nVarChar | 20 | [OTGG](OTGG.md) |  |  |
| 2 | `CardCode` | BP Code | nVarChar | 15 | - |  |  |
| 3 | `CardName` | BP Name | nVarChar | 200 | - |  |  |
| 4 | `GroupCode` | Group Code | nVarChar | 20 | - |  |  |
| 5 | `Industry` | Industry | Text | 16 | - |  |  |
| 6 | `validFor` | Active | VarChar | 1 | - |  | `A` = Active<br>`I` = Inactive |
| 7 | `CntctPrsn` | Contact Person | nVarChar | 50 | [OCPR](OCPR.md) |  |  |
| 8 | `Title` | Title | nVarChar | 10 | - |  |  |
| 9 | `Position` | Position | nVarChar | 90 | - |  |  |
| 10 | `E_Mail` | E-Mail | nVarChar | 100 | - |  |  |
| 11 | `Telephone` | Telephone | nVarChar | 50 | - |  |  |
| 12 | `Cellolar` | Mobile Phone | nVarChar | 50 | - |  |  |
| 13 | `Fax` | Fax | nVarChar | 50 | - |  |  |
| 14 | `Address` | Address | nVarChar | 100 | - |  |  |
| 15 | `Street` | Street | nVarChar | 100 | - |  |  |
| 16 | `Block` | Block | nVarChar | 100 | - |  |  |
| 17 | `City` | City | nVarChar | 100 | - |  |  |
| 18 | `ZipCode` | Zip Code | nVarChar | 20 | - |  |  |
| 19 | `County` | County | nVarChar | 100 | - |  |  |
| 20 | `State` | State | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 21 | `Country` | Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 22 | `Building` | Building/Floor/Room | Text | 16 | - |  |  |
| 23 | `LineNum` | Line Number | Int | 11 | - |  |  |
| 24 | `FirstName` | First Name | nVarChar | 50 | - |  |  |
| 25 | `MiddleName` | Middle Name | nVarChar | 50 | - |  |  |
| 26 | `LastName` | Last Name | nVarChar | 50 | - |  |  |
| 27 | `LicTradNum` | Federal Tax ID | nVarChar | 32 | - |  |  |
| 28 | `AddrType` | Address Type | nVarChar | 100 | - |  |  |
| 29 | `Address2` | Address Name 2 | nVarChar | 50 | - |  |  |
| 30 | `Address3` | Address Name 3 | nVarChar | 50 | - |  |  |
| 31 | `StreetNo` | Street No. | nVarChar | 100 | - |  |  |
| 32 | `AddressID` | Address ID | nVarChar | 50 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TargetCode, LineNum |
