# OVRT - Tax Invoice Report

- **Tabla:** OVRT
- **Descripción:** Tax Invoice Report
- **Cantidad de campos:** 22
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OVRT.html

## Campos (22)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TxInvRptNo` | Tax Invoice Rpt Number | nVarChar | 10 | - |  |  |
| 2 | `TxInvRptDt` | Tax Invoice Rpt Create Date | Date | 8 | - |  |  |
| 3 | `SupBPLId` | Supplier BPL ID | Int | 11 | - |  |  |
| 4 | `CardCode` | Receipt BP Code | nVarChar | 15 | - |  |  |
| 5 | `BaseAmt` | Total Base Amount(LC) | Num | 19.6 | - |  |  |
| 6 | `BlankNo` | Blank Before Total Base Amount | Int | 11 | - |  |  |
| 7 | `TaxAmt` | Total Tax Amount(LC) | Num | 19.6 | - |  |  |
| 8 | `Total` | Total Base + Total Tax | Num | 19.6 | - |  |  |
| 9 | `BPAddress` | Customer Pay to Address | nVarChar | 254 | - |  |  |
| 10 | `version` | Report Generation Version | nVarChar | 50 | - |  |  |
| 11 | `ReportType` | VAT: Tax Report Type ID | Int | 11 | [OKRT](OKRT.md) |  |  |
| 12 | `NTSApprov` | NTS Approved | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 13 | `NTSWebSite` | E-Tax Web Site | Int | 6 | [OTWS](OTWS.md) | -1 |  |
| 14 | `NTSeTaxNo` | E-Tax Number | nVarChar | 50 | - |  |  |
| 15 | `NTSApprNo` | NTS Approval Number | nVarChar | 50 | - |  |  |
| 16 | `Remarks` | Remarks | nVarChar | 254 | - |  |  |
| 17 | `OriNTSAppr` | Original NTS Approval Number | nVarChar | 50 | - |  |  |
| 18 | `CardName` | Receipt BP Code | nVarChar | 200 | - |  |  |
| 19 | `RptStatus` | Tax Invoice Report Status | VarChar | 1 | - | S | `S` = Saved<br>`C` = Canceled<br>`R` = Reversed |
| 20 | `OriTaxInvN` | Original Tax Invoice Number | nVarChar | 10 | - |  |  |
| 21 | `TxInvPrint` | Tax Invoice Report Print Type | VarChar | 1 | - | I | `A` = Aggregated<br>`I` = Individual |
| 22 | `Canceled` | Tax Invoice Report is Canceled or Not | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TxInvRptNo |
