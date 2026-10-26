# ELS1 - Vat Report Declaration Lines

- **Tabla:** ELS1
- **Descripción:** Vat Report Declaration Lines
- **Cantidad de campos:** 53
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ELS1.html

## Campos (53)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `RunId` | Run Number | Int | 11 | [OELS](OELS.md) |  |  |
| 2 | `VatViewAbs` | Vat View Abs Entry | Int | 11 | - |  |  |
| 3 | `Code` | Code | nVarChar | 8 | - |  |  |
| 4 | `Name` | Name | nVarChar | 50 | - |  |  |
| 5 | `SrcObjType` | Source Object Type | nVarChar | 20 | - |  |  |
| 6 | `DocNum` | Document Number | Int | 11 | - |  |  |
| 7 | `Category` | Category | VarChar | 1 | - |  |  |
| 8 | `IsEC` | EU | VarChar | 1 | - |  |  |
| 9 | `IsAcq` | Acquisition Tax Liable | VarChar | 1 | - |  |  |
| 10 | `VatPercent` | VAT Percent | Num | 19.6 | - |  |  |
| 11 | `EqPercent` | Equalization Percent | Num | 19.6 | - |  |  |
| 12 | `DocDate` | Posting Date | Date | 8 | - |  |  |
| 13 | `TaxDate` | Document Date | Date | 8 | - |  |  |
| 14 | `CANCELLED` | CANCELLED | VarChar | 1 | - |  |  |
| 15 | `BaseSum` | Base Sum | Num | 19.6 | - |  |  |
| 16 | `VatSum` | VAT Sum | Num | 19.6 | - |  |  |
| 17 | `EqSum` | Equalization Sum | Num | 19.6 | - |  |  |
| 18 | `DeductSum` | Deduct VAT Sum | Num | 19.6 | - |  |  |
| 19 | `SrcObjAbs` | Source Object Internal ID | Int | 11 | - |  |  |
| 20 | `BaseObjTyp` | Base Object Type | nVarChar | 20 | - |  |  |
| 21 | `TaxAbs` | Internal Number | Int | 11 | - |  |  |
| 22 | `InvNum` | Invoice Document Number | Int | 11 | - |  |  |
| 23 | `InvDate` | Invoice Date | Date | 8 | - |  |  |
| 24 | `InvAmnt` | Invoice Amount | Num | 19.6 | - |  |  |
| 25 | `InvVatAmnt` | Invoice Vat Amount | Num | 19.6 | - |  |  |
| 26 | `VendorRef` | BP Name | nVarChar | 200 | - |  |  |
| 27 | `BaseSumSc` | Base Sum (SC) | Num | 19.6 | - |  |  |
| 28 | `VatSumSc` | VAT Sum (SC) | Num | 19.6 | - |  |  |
| 29 | `EqSumSC` | Equalization Sum (SC) | Num | 19.6 | - |  |  |
| 30 | `DedctSumSC` | Deduct VAT Sum (SC) | Num | 19.6 | - |  |  |
| 31 | `TaxType` | Tax Type | VarChar | 1 | - |  |  |
| 32 | `CrditDebit` | Credit Or Debit Transaction | VarChar | 1 | - |  |  |
| 33 | `CardCode` | BP Code | nVarChar | 15 | - |  |  |
| 34 | `CardName` | BP Name | nVarChar | 200 | - |  |  |
| 35 | `ReportType` | Report Type | Int | 11 | - |  |  |
| 36 | `SrcLineNum` | Source Row Number | Int | 11 | - |  |  |
| 37 | `VatDate` | VAT Date | Date | 8 | - |  |  |
| 38 | `VatIdUnCmp` | Unified Federal Tax ID | nVarChar | 32 | - |  |  |
| 39 | `DocLicTrad` | Document Federal Tax ID | nVarChar | 32 | - |  |  |
| 40 | `BPLicTrad` | BP Federal Tax ID | nVarChar | 32 | - |  |  |
| 41 | `AddID` | ID No. 2 | nVarChar | 64 | - |  |  |
| 42 | `OrdinLNum` | Ordial Num (BTF & Canceled) | Int | 11 | - |  |  |
| 43 | `EqBaseSum` | Equalization Base Sum | Num | 19.6 | - |  |  |
| 44 | `IsSplitPay` | Split Payment | VarChar | 1 | - |  |  |
| 45 | `CAOutCode` | Custom Acct Output Tax Code | nVarChar | 8 | - |  |  |
| 46 | `CABasSum` | Custom Acct Reverse Base Sum | Num | 19.6 | - |  |  |
| 47 | `CABasSumSc` | Custom Acct Reverse Base SumSC | Num | 19.6 | - |  |  |
| 48 | `CAVatSum` | Custom Acct Reverse VAT Sum | Num | 19.6 | - |  |  |
| 49 | `CAVatSumSc` | Custom Acct Reverse VAT SumSC | Num | 19.6 | - |  |  |
| 50 | `VatSumSrc` | VAT Sum Source | VarChar | 1 | - |  |  |
| 51 | `VatType` | Type of VAT | Int | 11 | - |  |  |
| 52 | `GoddsShip` | Goods Shipment | VarChar | 1 | - |  |  |
| 53 | `ServSupply` | Service Supply | VarChar | 1 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | RunId, VatViewAbs, Code, Category |
