# OSTA - Sales Tax Authorities

- **Tabla:** OSTA
- **Descripción:** Sales Tax Authorities
- **Cantidad de campos:** 36
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSTA.html

## Campos (36)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Code | nVarChar | 8 | - |  |  |
| 2 | `Name` | Name | nVarChar | 100 | - |  |  |
| 3 | `Rate` | Rate | Num | 19.6 | - |  |  |
| 4 | `SalesTax` | Sales Tax Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 5 | `UseTax` | Use Tax Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 6 | `Type` | Type | Int | 11 | [OSTT](OSTT.md) |  |  |
| 7 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 8 | `PurchTax` | Purchasing Tax Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 9 | `deferrAcct` | Deferred Tax Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 10 | `NonDdctPrc` | Non Deductible % | Num | 19.6 | - |  |  |
| 11 | `NonDdctAct` | Non Deductible Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 12 | `TaxInPrice` | Included in Price | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 13 | `Exempt` | Exempt | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 14 | `APExpAct` | Purchasing Tax Expense Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 15 | `ARExpAct` | Sales Tax Expense Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 16 | `CredBala` | Credit Balance: Raw Material | Num | 19.6 | - |  |  |
| 17 | `CredFG` | Credit for Finished Goods | Num | 19.6 | - |  |  |
| 18 | `CredCG` | Credit for Capital Goods | Num | 19.6 | - |  |  |
| 19 | `InGrossRev` | Included in Gross Revenue | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 20 | `EfctDate` | Effective From | Date | 8 | - |  |  |
| 21 | `SvcTaxCr` | Credit for Service Tax | Num | 19.6 | - |  |  |
| 22 | `MinAmount` | Min. Taxable Amount | Num | 19.6 | - |  |  |
| 23 | `MaxAmount` | Max. Taxable Amount | Num | 19.6 | - |  |  |
| 24 | `FlatAmount` | Flat Tax Amount | Num | 19.6 | - |  |  |
| 25 | `TextCode` | Text Code | Int | 6 | - |  |  |
| 26 | `UnencumTax` | Unencumbered Tax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 27 | `TaxOnRI` | Tax On Reserve Invoice | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 28 | `DIOTRptTyp` | DIOT Report Type | VarChar | 1 | - |  | `A` = 15% or 16% VAT<br>`B` = 15% or 16% VAT on Import<br>`C` = Exempt on Import<br>`D` = 0% VAT<br>`E` = Exempt<br>`F` = VAT on Returns, Discounts, and Rebates<br>`G` = Stimulus for Northern Border Region<br>`H` = IEPS Tax<br>`I` = Stimulus for Southern Border Region |
| 29 | `IsSystem` | Is System Tax Jurisdiction | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 30 | `RvsCrgPrc` | Reverse Charge % | Num | 19.6 | - |  |  |
| 31 | `InFirstIns` | Included in First Installment | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 32 | `SaleTaxRCM` | Sales Tax RCM Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 33 | `SaleRCMClr` | Sales Tax RCM Clearing Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 34 | `VatExempt` | Apply VAT Exemption | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 35 | `VatExmPrc` | VAT Exemption % | Num | 19.6 | - |  |  |
| 36 | `VatExmBase` | Base VAT % | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code, Type |
