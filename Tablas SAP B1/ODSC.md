# ODSC - Bank Codes

- **Tabla:** ODSC
- **Descripción:** Bank Codes
- **Cantidad de campos:** 24
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ODSC.html

## Campos (24)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `BankCode` | Bank Code | nVarChar | 30 | - |  |  |
| 2 | `BankName` | Bank Name | nVarChar | 250 | - |  |  |
| 3 | `DfltAcct` | Account for Outgoing Checks | nVarChar | 50 | - |  |  |
| 4 | `DfltBranch` | Branch for Outgoing Checks | nVarChar | 50 | - |  |  |
| 5 | `NextChckNo` | Next Check Number | Int | 11 | - |  |  |
| 6 | `Locked` | Locked | VarChar | 1 | - | N | `N` = Changeable<br>`Y` = Locked |
| 7 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 8 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 9 | `SwiftNum` | BIC/SWIFT Code | nVarChar | 50 | - |  |  |
| 10 | `IBAN` | IBAN | nVarChar | 50 | - |  |  |
| 11 | `CountryCod` | Country/Region Code | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 12 | `PostOffice` | Post Office | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 13 | `AliasName` | Alias Name | nVarChar | 50 | - |  |  |
| 14 | `AbsEntry` | Absolute entry | Int | 11 | - |  |  |
| 15 | `DfltActKey` | Default Bank Account Key | Int | 11 | [DSC1](DSC1.md) |  |  |
| 16 | `NextNum` | Our Number in Next Boleto | Int | 11 | - |  |  |
| 17 | `BsPstDate` | Posting Date Definition | VarChar | 1 | - | C | `S` = Statement Date<br>`L` = Row Date<br>`V` = Due Date<br>`C` = Current Date |
| 18 | `BsValDate` | Due Date Definition | VarChar | 1 | - | C | `S` = Statement Date<br>`L` = Row Date<br>`V` = Due Date<br>`C` = Current Date |
| 19 | `BnkOpCode` | Bank Operation Code List | Int | 11 | [OBOC](OBOC.md) |  |  |
| 20 | `BsDocDate` | Document Date Definition | VarChar | 1 | - | C | `S` = Statement Date<br>`L` = Row Date<br>`V` = Due Date<br>`C` = Current Date |
| 21 | `TaxIdNum` | Federal Tax ID | nVarChar | 32 | - |  |  |
| 22 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 23 | `EnDfltAcct` | Encryption of Default Account | Text | 16 | - |  |  |
| 24 | `DigPayment` | Digital Payments | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| SECONDARY | Yes | CountryCod, BankCode |
