# AWHT - Withholding Tax

- **Tabla:** AWHT
- **Descripción:** Withholding Tax
- **Cantidad de campos:** 64
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AWHT.html

## Campos (64)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WTCode` | WTax Code | nVarChar | 4 | - |  |  |
| 2 | `WTName` | WTax Name | nVarChar | 50 | - |  |  |
| 3 | `Rate` | Rate | Num | 19.6 | - |  |  |
| 4 | `EffecDate` | Effective From | Date | 8 | - |  |  |
| 5 | `Category` | Category | VarChar | 1 | - | P | `I` = Invoice<br>`P` = Payment |
| 6 | `BaseType` | Base Type | VarChar | 1 | - | N | `G` = Gross<br>`N` = Net<br>`V` = VAT<br>`U` = UoM |
| 7 | `PrctBsAmnt` | % Base Amount | Num | 19.6 | - |  |  |
| 8 | `OffclCode` | Official Code | nVarChar | 15 | - |  |  |
| 9 | `Account` | Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 10 | `MinTaxAmt` | Minimum Taxable Amount | Num | 19.6 | - |  |  |
| 11 | `IsPrgrss` | Progressive Tax | VarChar | 1 | - | N | `Y` = Progressive Tax<br>`N` = Not Progressive Tax |
| 12 | `Type` | Withholding Type | VarChar | 1 | - | V | `V` = VAT Withholding<br>`I` = Income Tax Withholding |
| 13 | `RoundType` | Rounding Type | VarChar | 1 | - | C | `T` = Truncated AU<br>`C` = Commercial Values |
| 14 | `WTTypeId` | Type | Int | 11 | [OWTT](OWTT.md) |  |  |
| 15 | `WTCurrency` | Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 16 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 17 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 18 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 19 | `Section` | Section | Int | 11 | [OSEC](OSEC.md) |  |  |
| 20 | `Threshold` | Cumulative Threshold | Num | 19.6 | - |  |  |
| 21 | `Surcharge` | Surcharge | Num | 19.6 | - |  |  |
| 22 | `Concess` | Concessional | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 23 | `Assessee` | Assessee | Int | 11 | [ONOA](ONOA.md) |  |  |
| 24 | `ApTdsAcc` | A/P TDS Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 25 | `ApSurAcc` | A/P Surcharge Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 26 | `ApCessAcc` | A/P Cess Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 27 | `ApHscAcc` | A/P HSC Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 28 | `ArTdsAcc` | A/R TDS Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 29 | `ArSurAcc` | A/R Surcharge Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 30 | `ArCessAcc` | A/R Cess Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 31 | `ArHscAcc` | A/R HSC Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 32 | `Location` | Location | Int | 11 | [OLCT](OLCT.md) |  |  |
| 33 | `ReturnType` | Return Type | VarChar | 1 | - |  | `A` = 26<br>`B` = 27 |
| 34 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 35 | `Inactive` | Inactive | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 36 | `InCSTCode` | CST Code Incoming | Int | 11 | [OTSC](OTSC.md) | -1 |  |
| 37 | `OutCSTCode` | CST Code Outgoing | Int | 11 | [OTSC](OTSC.md) | -1 |  |
| 38 | `CalBaseN` | Nature of Calculation Base | nVarChar | 2 | [OBSI](OBSI.md) |  |  |
| 39 | `PymntRsnCd` | Payment Reason Code | nVarChar | 3 | [OSWA](OSWA.md) |  |  |
| 40 | `DIOTRpt` | DIOT Report | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 41 | `TDSType` | TDS Type | VarChar | 1 | - |  | `E` = eTDS<br>`D` = GST TDS<br>`C` = GST TCS |
| 42 | `ApIgstAcc` | A/P IGST Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 43 | `ApCgstAcc` | A/P CGST Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 44 | `ApSgstAcc` | A/P SGST Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 45 | `ArIgstAcc` | A/R IGST Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 46 | `ArCgstAcc` | A/R CGST Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 47 | `ArSgstAcc` | A/R SGST Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 48 | `ApUtgstAcc` | A/P UTGST Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 49 | `ApCsgstAcc` | A/P Cess GST Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 50 | `ArUtgstAcc` | A/R UTGST Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 51 | `ArCsgstAcc` | A/R Cess GST Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 52 | `TransThres` | Transaction Threshold | Num | 19.6 | - | 0 |  |
| 53 | `EBWTaxCate` | Withholding Tax Category | Int | 11 | [OWHC](OWHC.md) |  |  |
| 54 | `ArTcsInAcc` | A/R TCS Interim Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 55 | `ArSurInAcc` | A/R Surcharge Interim Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 56 | `ArCesInAcc` | A/R Cess Interim Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 57 | `ArHscInAcc` | A/R HSC Interim Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 58 | `ApTcsInAcc` | A/P TCS Interim Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 59 | `ApSurInAcc` | A/P Surcharge Interim Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 60 | `ApCesInAcc` | A/P Cess Interim Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 61 | `ApHscInAcc` | A/P HSC Interim Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 62 | `LnWTInAcc` | Interim Account for Tax | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 63 | `NoDedThrsh` | Apply Tax Exemption After Threshold | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 64 | `UseInAPDPR` | Use in A/P Down Payment Requests | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WTCode, LogInstanc |
