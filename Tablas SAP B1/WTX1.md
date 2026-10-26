# WTX1 - WTax Transactions - Rows

- **Tabla:** WTX1
- **Descripción:** WTax Transactions - Rows
- **Cantidad de campos:** 54
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WTX1.html

## Campos (54)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal ID | Int | 11 | [OWTX](OWTX.md) |  |  |
| 2 | `LineSeq` | Row Sequence | Int | 11 | - |  |  |
| 3 | `SrcArrType` | Source Array Type | Int | 11 | - | -1 | `-1` = Default<br>`1` = Main<br>`12` = Array 1<br>`13` = Array 2<br>`14` = Array 3 |
| 4 | `SrcLineNum` | Source Row Number | Int | 11 | - | -1 |  |
| 5 | `SrcGrpNum` | Source Group Number | Int | 11 | - | -1 | `-1` = Default<br>`0` = Group 1<br>`1` = Group 2<br>`2` = Group 3 |
| 6 | `BaseObjTyp` | Base Object Type | nVarChar | 20 | - | -1 |  |
| 7 | `BaseAbs` | Base Document Internal No. | Int | 11 | - | -1 |  |
| 8 | `BaseArrTyp` | Base Array Type | Int | 11 | - | -1 | `-1` = Default<br>`1` = Main<br>`12` = Array 1<br>`13` = Array 2<br>`14` = Array 3<br>`15` = Array 4<br>`16` = Array 5<br>`17` = Array 6<br>`18` = Array 7<br>`24` = Array 13 |
| 9 | `BaseLinNum` | Base Row Number | Int | 11 | - | -1 |  |
| 10 | `BaseGrpNum` | Base Group No. | Int | 11 | - | -1 | `-1` = Default<br>`0` = Group 1<br>`1` = Group 2<br>`2` = Group 3 |
| 11 | `WTaxAbsId` | Tax Code ID | nVarChar | 8 | - |  |  |
| 12 | `Account` | Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 13 | `Rate` | Rate | Num | 19.6 | - |  |  |
| 14 | `Exemption` | Exemption Rate | Num | 19.6 | - |  |  |
| 15 | `BaseType` | Base Type | VarChar | 1 | - | N | `N` = Net<br>`V` = VAT<br>`G` = Gross<br>`H` = Gross - VAT |
| 16 | `BaseNetSum` | Base Net Sum | Num | 19.6 | - |  |  |
| 17 | `BaseNetSC` | Base Net Sum (SC) | Num | 19.6 | - |  |  |
| 18 | `BaseNetFC` | Base Net Sum (FC) | Num | 19.6 | - |  |  |
| 19 | `BaseVatSum` | Base VAT Sum | Num | 19.6 | - |  |  |
| 20 | `BaseVatSC` | Base VAT Sum (SC) | Num | 19.6 | - |  |  |
| 21 | `BaseVatFC` | Base VAT Sum (FC) | Num | 19.6 | - |  |  |
| 22 | `AccBaseSum` | Accumulated Sum | Num | 19.6 | - |  |  |
| 23 | `AccBaseSC` | Accumulated Sum (SC) | Num | 19.6 | - |  |  |
| 24 | `AccBaseFC` | Accumulated Sum (FC) | Num | 19.6 | - |  |  |
| 25 | `AccWTaxSum` | Accumulated WTax Sum | Num | 19.6 | - |  |  |
| 26 | `AccWTaxSC` | Accumulated WTax Sum (SC) | Num | 19.6 | - |  |  |
| 27 | `AccWTaxFC` | Accumulated WTax Sum (FC) | Num | 19.6 | - |  |  |
| 28 | `TxblSum` | Taxable Sum | Num | 19.6 | - |  |  |
| 29 | `TxblSumSc` | Taxable Sum (SC) | Num | 19.6 | - |  |  |
| 30 | `TxblSumFc` | Taxable Sum (FC) | Num | 19.6 | - |  |  |
| 31 | `WTaxSum` | WTax Sum | Num | 19.6 | - |  |  |
| 32 | `WTaxSumSc` | WTax Sum (SC) | Num | 19.6 | - |  |  |
| 33 | `WTaxSumFc` | WTax Sum (FC) | Num | 19.6 | - |  |  |
| 34 | `ApplSum` | Applied Sum | Num | 19.6 | - |  |  |
| 35 | `ApplSumSc` | Applied Sum (SC) | Num | 19.6 | - |  |  |
| 36 | `ApplSumFc` | Applied Sum (FC) | Num | 19.6 | - |  |  |
| 37 | `CrditDebit` | Credit or Debit Transaction | VarChar | 1 | - |  | `C` = Credit<br>`D` = Debit |
| 38 | `PostingTyp` | Sales or Purchase | VarChar | 1 | - | N | `N` = None<br>`R` = Sales<br>`P` = Purchase |
| 39 | `Category` | Category | VarChar | 1 | - | P | `I` = Invoice<br>`P` = Payment |
| 40 | `WTTypeId` | Type | Int | 11 | - |  |  |
| 41 | `WhtType` | Withholding Type | VarChar | 1 | - | V | `V` = VAT Withholding<br>`G` = Gross Income Withholding<br>`N` = Income Tax Withholding<br>`S` = Social Security Withholding<br>`I` = Industry Specific Withholding<br>`D` = District Specific Withholding |
| 42 | `FmlId` | Formula ID | Int | 11 | - |  |  |
| 43 | `BaseMin` | Min. Amount | Num | 19.6 | - |  |  |
| 44 | `BaseMinSc` | Min. Amount (SC) | Num | 19.6 | - |  |  |
| 45 | `BaseMinFc` | Min. Amount (FC) | Num | 19.6 | - |  |  |
| 46 | `ResMin` | Min.Ret./Perc. Amount | Num | 19.6 | - |  |  |
| 47 | `ResMinSc` | Min.Ret./Perc. Amount (SC) | Num | 19.6 | - |  |  |
| 48 | `ResMinFc` | Min.Ret./Perc. Amount (FC) | Num | 19.6 | - |  |  |
| 49 | `AddBas` | Add to Base Amount | Num | 19.6 | - |  |  |
| 50 | `AddBasSc` | Add to Base Amount (SC) | Num | 19.6 | - |  |  |
| 51 | `AddBasFc` | Add to Base Amount (FC) | Num | 19.6 | - |  |  |
| 52 | `ABWVAT` | Add to Base without VAT Amount | Num | 19.6 | - |  |  |
| 53 | `ABWVATSc` | Add to Base without VAT Amount (SC) | Num | 19.6 | - |  |  |
| 54 | `ABWVATFc` | Add to Base without VAT Amount (FC) | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineSeq |
