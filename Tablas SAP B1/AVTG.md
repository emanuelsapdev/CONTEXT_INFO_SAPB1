# AVTG - Tax Definition

- **Tabla:** AVTG
- **Descripción:** Tax Definition
- **Cantidad de campos:** 73
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AVTG.html

## Campos (73)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Code | nVarChar | 8 | - |  |  |
| 2 | `Name` | Name | nVarChar | 50 | - |  |  |
| 3 | `Rate` | Rate % | Num | 19.6 | - |  |  |
| 4 | `EffecDate` | Effective from | Date | 8 | - |  |  |
| 5 | `Category` | Category | VarChar | 1 | - | O | `O` = Output Tax<br>`I` = Input Tax |
| 6 | `Account` | Tax Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 7 | `Locked` | Locked | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 9 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 10 | `IsEC` | EU | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 11 | `Indicator` | Triangular Deal | VarChar | 1 | [OIND](OIND.md) |  |  |
| 12 | `AcqstnRvrs` | Acquisition/Reverse | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 13 | `NonDedct` | Non-Deductible % | Num | 19.6 | - |  |  |
| 14 | `AcqsTax` | Acquisition Tax Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 15 | `GoddsShip` | Goods Shipment | VarChar | 1 | [OGSP](OGSP.md) |  |  |
| 16 | `NonDedAcc` | Non-Deductible Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 17 | `DeferrAcc` | Deferred Tax Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 18 | `EquVatPr` | Equalization Tax % | Num | 19.6 | - |  |  |
| 19 | `ReportCode` | Group Description | nVarChar | 100 | - |  |  |
| 20 | `FixdAssts` | Fixed Assets Flag | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 21 | `CalcMethod` | Calculation Method | VarChar | 1 | - | R | `R` = Rate<br>`F` = Fixed |
| 22 | `TaxType` | Tax Type (VAT or Stamp) | VarChar | 1 | - | V | `V` = VAT<br>`S` = Stamp |
| 23 | `FixedAmnt` | Fixed Amount (LC) | Num | 19.6 | - |  |  |
| 24 | `ExtCode` | External Code | nVarChar | 10 | - |  |  |
| 25 | `Correction` | Correction | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 26 | `VatCrctn` | VAT Correction | nVarChar | 8 | [OVTG](OVTG.md) |  |  |
| 27 | `RetVatCode` | Returning VAT Code | nVarChar | 8 | - |  |  |
| 28 | `RepType` | Report Type | Int | 11 | [OKRT](OKRT.md) |  |  |
| 29 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 30 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 31 | `TaxCtgr` | Tax Type (Annual List) | nVarChar | 6 | - | E | `E` = Excluded<br>`T` = Taxable<br>`X` = Exempt<br>`N` = Not Taxable<br>`N31` = N3.1 - Not Taxable - exports<br>`N32` = N3.2 - Not Taxable - intra-community sales<br>`N33` = N3.3 - Not Taxable - sales to San Marino<br>`N34` = N3.4 - Not Taxable - operations similar to export sales<br>`N35` = N3.5 - Not Taxable - due to tax exemption letter<br>`N36` = N3.6 - Not Taxable - other transactions<br>`G` = Gross Profit<br>`R` = Reverse Charge<br>`R61` = N6.1 - Reverse Charge - disposal of scrap and other recycled materials<br>`R62` = N6.2 - Accounting Reversal - sale of gold and pure silver<br>`R63` = N6.3 - Reverse Charge - subcontracting in the construction sector<br>`R64` = N6.4 - Reverse Charge - sales of buildings<br>`R65` = N6.5 - Reverse Charge - sales of cell phones<br>`R66` = N6.6 - Reverse Charge - sales of electronic products<br>`R67` = N6.7 - Reverse Charge - services of the construction and related sectors<br>`R68` = N6.8 - Reverse Charge - energy sector operations<br>`R69` = N6.9 - Reverse Charge - other cases<br>`U` = Tourism<br>`A` = Taxable - Article 162<br>`B` = Taxable - Article 173 point 5<br>`C` = Taxable - Construction<br>`D` = Taxable - Expected Confirmation<br>`F` = Taxable - Gross<br>`I` = Taxable - Import<br>`Y` = Taxable - Import from EAEU<br>`L` = Taxable - Late Export<br>`O` = Taxable - Not Confirmed<br>`S` = Taxable - Real Estate<br>`W` = Taxable - Sale of Company<br>`H` = Excluded Art. 15<br>`J` = Not Subject<br>`J21` = N2.1 - Not Subject - to VAT under articles from 7 to 7-septies of DPR 633/72<br>`J22` = N2.2 - Not Subject - other cases<br>`K` = Paid in other EU country<br>`M` = Taxable - Article 151 point 1<br>`P` = Taxable - Article 170 point 3<br>`V` = Taxable - Fixed Assets<br>`Q` = Taxable - Tax Free |
| 32 | `EquAccount` | Equalization Tax Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 33 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 34 | `IsIGIC` | IGIC | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 35 | `ServSupply` | Service Supply | VarChar | 1 | [OSSP](OSSP.md) |  |  |
| 36 | `Inactive` | Inactive | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 37 | `TaxCtgrBL` | Tax Type (Black List) | VarChar | 1 | - | E | `E` = Excluded<br>`T` = Taxable<br>`X` = Exempt<br>`N` = Not Taxable<br>`S` = Non-Subject |
| 38 | `R349Code` | Report 349 Code | Int | 11 | - | 0 | `0`<br>`1` = E<br>`2` = A<br>`3` = T<br>`4` = S<br>`5` = I<br>`6` = M<br>`7` = H |
| 39 | `VatRevAcc` | VAT in Revenue Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 40 | `CashDisAcc` | Cash Discount Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 41 | `DpmTaxOAcc` | Down Paymnt Tax Offset Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 42 | `VatDedAcc` | VAT Deductible Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 43 | `CstmExpAcc` | Customs VAT Expense Account | nVarChar | 15 | - |  |  |
| 44 | `CstmAlcAcc` | Customs VAT Allocation Account | nVarChar | 15 | - |  |  |
| 45 | `TaxRegion` | Tax Country Region | nVarChar | 5 | - | PT | `PT` = Continental Portugal<br>`PT-AC` = Azores Islands<br>`PT-MA` = Madeira Islands |
| 46 | `ExemReason` | Tax Exemption Reason | nVarChar | 3 | - |  |  |
| 47 | `Agent` | Agent | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 48 | `OpCode` | Tax Operation Code | nVarChar | 7 | - |  |  |
| 49 | `Export` | Export | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 50 | `Section` | VAT Section | nVarChar | 3 | - |  |  |
| 51 | `SplitPaymt` | Split Payment | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 52 | `SplitPayAc` | Split Payment Account | nVarChar | 15 | - |  |  |
| 53 | `TaxAgent` | Tax Agent (Section 3) | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 54 | `SectionLim` | VAT Section (under limit) | nVarChar | 3 | - |  |  |
| 55 | `VatSubjCod` | VAT Subject Code | nVarChar | 10 | - |  |  |
| 56 | `VatType` | Type of VAT | Int | 11 | - | -1 |  |
| 57 | `VatCategor` | VAT Category | Int | 11 | - | -1 |  |
| 58 | `Parag44` | Paragraph 44 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 59 | `ProrataDed` | Pro-rata deductible | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 60 | `ExcFrmTaxS` | Exclude from Tax Summary Report Total A/R or A/P Net Amounts | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 61 | `CstmActing` | Customer Accounting | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 62 | `CstmActOut` | Customer Accounting Corresponding Tax Code | nVarChar | 8 | - |  |  |
| 63 | `StdTaxCode` | Standard Tax Code | nVarChar | 35 | - |  |  |
| 64 | `AcqRevTax` | Acquisition/Reverse Corresponding Tax Code | nVarChar | 8 | - |  |  |
| 65 | `ExReasonHU` | Tax Exemption Reason | nVarChar | 30 | - |  |  |
| 66 | `ExRemarkHU` | Tax Exemption Remark | nVarChar | 50 | - |  |  |
| 67 | `EBVatCateg` | VAT Category | Int | 11 | - |  |  |
| 68 | `SAFTTaxCod` | SAF-T Tax Code | nVarChar | 10 | - | NOR | `RED` = Reduced Tax<br>`INT` = Middle Tax<br>`NOR` = Normal Tax<br>`ISE` = Exempt<br>`OUT` = Others |
| 69 | `EBVatExCau` | VAT Exemption Cause | Int | 11 | [OVEC](OVEC.md) |  |  |
| 70 | `VatClasTyp` | VAT Expense Class. Type | Int | 11 | [OECP](OECP.md) |  |  |
| 71 | `VatClasCat` | VAT Expense Class. Category | Int | 11 | [OECC](OECC.md) |  |  |
| 72 | `SAFTTxCdEx` | SAF-T Tax Code | nVarChar | 10 | [OSTX](OSTX.md) | NOR |  |
| 73 | `VATEX` | VAT Exemption Reason | nVarChar | 32 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code, LogInstanc |
| GROUP_NAME | No | Name, LogInstanc |
