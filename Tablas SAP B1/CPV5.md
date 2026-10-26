# CPV5 - A/P Correction Invoice Reversal - WTax

- **Tabla:** CPV5
- **Descripción:** A/P Correction Invoice Reversal - WTax
- **Cantidad de campos:** 161
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CPV5.html

## Campos (161)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Numerator | Int | 11 | [OCPV](OCPV.md) |  |  |
| 2 | `WTCode` | WT Code | nVarChar | 4 | [OWHT](OWHT.md) |  |  |
| 3 | `Rate` | Rate | Num | 19.6 | - |  |  |
| 4 | `TaxbleAmnt` | Taxable Amount | Num | 19.6 | - |  |  |
| 5 | `TxblAmntSC` | Taxable Amount (SC) | Num | 19.6 | - |  |  |
| 6 | `TxblAmntFC` | Taxable Amount (FC) | Num | 19.6 | - |  |  |
| 7 | `WTAmnt` | WT Amount | Num | 19.6 | - |  |  |
| 8 | `WTAmntSC` | WT Amount (SC) | Num | 19.6 | - |  |  |
| 9 | `WTAmntFC` | WT Amount (FC) | Num | 19.6 | - |  |  |
| 10 | `ApplAmnt` | Applied WT Amount | Num | 19.6 | - |  |  |
| 11 | `ApplAmntSC` | Applied WTax Amount (SC) | Num | 19.6 | - |  |  |
| 12 | `ApplAmntFC` | Applied WTax Amount (FC) | Num | 19.6 | - |  |  |
| 13 | `Category` | Category | VarChar | 1 | - |  | `P` = Payment<br>`I` = Invoice |
| 14 | `Criteria` | WT Criteria | VarChar | 1 | - |  | `Y` = Accrual<br>`N` = Cash |
| 15 | `Account` | G/L Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 16 | `Type` | Withholding Type | VarChar | 1 | - |  | `V` = VAT Withholding<br>`I` = Income Tax Withholding |
| 17 | `RoundType` | Rounding Type | VarChar | 1 | - |  | `T` = Truncated<br>`C` = Commercial Values<br>`N` = No Rounding |
| 18 | `BaseType` | Base Type | VarChar | 1 | - |  | `G` = Gross<br>`N` = Net<br>`V` = VAT<br>`U` = UoM |
| 19 | `BaseAbsEnt` | Base Abs Entry | Int | 11 | - | -1 |  |
| 20 | `BaseLine` | Base Line | Int | 11 | - |  |  |
| 21 | `BaseNum` | Base Document Type | Int | 11 | - | -1 | `-1`<br>`0`<br>`163` = A/P Correction Invoice |
| 22 | `LineNum` | Line Number | Int | 11 | - |  |  |
| 23 | `BaseRef` | Base Document Reference | Int | 11 | - |  |  |
| 24 | `Status` | Status | VarChar | 1 | - | O | `O` = Open<br>`C` = Closed |
| 25 | `TrgType` | Target Document Type | Int | 11 | - |  |  |
| 26 | `TrgAbsEntr` | Target Abs. Entry | Int | 11 | - | -1 |  |
| 27 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 28 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 164 |  |
| 29 | `Doc1LineNo` | DOC1 Line Number | Int | 11 | - | -1 |  |
| 30 | `WtLineType` | WT Line Type | VarChar | 1 | - | D | `D` = Document Level WTax<br>`L` = Row Level WTax |
| 31 | `TxblCurr` | Taxable Currency from Doc Line | nVarChar | 3 | - |  |  |
| 32 | `DtblCurr` | Deductible Currency | nVarChar | 3 | - |  |  |
| 33 | `DtblRate` | Rate for Deductible Amount | Num | 19.6 | - |  |  |
| 34 | `txblRate` | Rate for Taxable Amount | Num | 19.6 | - |  |  |
| 35 | `DtblAmount` | Deductible Amount | Num | 19.6 | - |  |  |
| 36 | `TdsAcc` | TDS Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 37 | `SurAcc` | Surcharge Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 38 | `CessAcc` | Cess Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 39 | `HscAcc` | HSC Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 40 | `TdsRate` | TDS Rate | Num | 19.6 | - |  |  |
| 41 | `SurRate` | Surcharge Rate | Num | 19.6 | - |  |  |
| 42 | `CessRate` | Cess Rate | Num | 19.6 | - |  |  |
| 43 | `HscRate` | HSC Rate | Num | 19.6 | - |  |  |
| 44 | `TdsBAmt` | TDS Base Amount | Num | 19.6 | - |  |  |
| 45 | `TdsBAmtSC` | TDS Base Amount (SC) | Num | 19.6 | - |  |  |
| 46 | `TdsBAmtFC` | TDS Base Amount (FC) | Num | 19.6 | - |  |  |
| 47 | `SurBAmt` | Surcharge Base Amount | Num | 19.6 | - |  |  |
| 48 | `SurBAmtSC` | Surcharge Base Amount (SC) | Num | 19.6 | - |  |  |
| 49 | `SurBAmtFC` | Surcharge Base Amount (FC) | Num | 19.6 | - |  |  |
| 50 | `CessBAmt` | Cess Base Amount | Num | 19.6 | - |  |  |
| 51 | `CessBAmtSC` | Cess Base Amount (SC) | Num | 19.6 | - |  |  |
| 52 | `CessBAmtFC` | Cess Base Amount (FC) | Num | 19.6 | - |  |  |
| 53 | `HscBAmt` | HSC Base Amount | Num | 19.6 | - |  |  |
| 54 | `HscBAmtSC` | HSC Base Amount (SC) | Num | 19.6 | - |  |  |
| 55 | `HscBAmtFC` | HSC Base Amount (FC) | Num | 19.6 | - |  |  |
| 56 | `TdsAmnt` | TDS Tax Amount | Num | 19.6 | - |  |  |
| 57 | `TdsAmntSC` | TDS Tax Amount (SC) | Num | 19.6 | - |  |  |
| 58 | `TdsAmntFC` | TDS Tax Amount (FC) | Num | 19.6 | - |  |  |
| 59 | `SurAmnt` | Surcharge Tax Amount | Num | 19.6 | - |  |  |
| 60 | `SurAmntSC` | Surcharge Tax Amount (SC) | Num | 19.6 | - |  |  |
| 61 | `SurAmntFC` | Surcharge Tax Amount (FC) | Num | 19.6 | - |  |  |
| 62 | `CessAmnt` | Cess Tax Amount | Num | 19.6 | - |  |  |
| 63 | `CessAmntSC` | Cess Tax Amount (SC) | Num | 19.6 | - |  |  |
| 64 | `CessAmntFC` | Cess Tax Amount (FC) | Num | 19.6 | - |  |  |
| 65 | `HscAmnt` | HSC Tax Amount | Num | 19.6 | - |  |  |
| 66 | `HscAmntSC` | HSC Tax Amount (SC) | Num | 19.6 | - |  |  |
| 67 | `HscAmntFC` | HSC Tax Amount (FC) | Num | 19.6 | - |  |  |
| 68 | `TdsAppl` | Applied TDS Amount | Num | 19.6 | - |  |  |
| 69 | `TdsApplSC` | Applied TDS Amount (SC) | Num | 19.6 | - |  |  |
| 70 | `TdsApplFC` | Applied TDS Amount (FC) | Num | 19.6 | - |  |  |
| 71 | `SurAppl` | Applied Surcharge Amount | Num | 19.6 | - |  |  |
| 72 | `SurApplSC` | Applied Surcharge Amount (SC) | Num | 19.6 | - |  |  |
| 73 | `SurApplFC` | Applied Surcharge Amount (FC) | Num | 19.6 | - |  |  |
| 74 | `CessAppl` | Applied Cess Amount | Num | 19.6 | - |  |  |
| 75 | `CessApplSC` | Applied Cess Amount (SC) | Num | 19.6 | - |  |  |
| 76 | `CessApplFC` | Applied Cess Amount (FC) | Num | 19.6 | - |  |  |
| 77 | `HscAppl` | Applied HSC Amount | Num | 19.6 | - |  |  |
| 78 | `HscApplSC` | Applied HSC Amount (SC) | Num | 19.6 | - |  |  |
| 79 | `HscApplFC` | Applied HSC Amount (FC) | Num | 19.6 | - |  |  |
| 80 | `BatchNum` | Journal Voucher No. | Int | 11 | - |  |  |
| 81 | `InCSTCode` | CST Code Incoming | nVarChar | 2 | - |  |  |
| 82 | `OutCSTCode` | CST Code Outgoing | nVarChar | 2 | - |  |  |
| 83 | `DpmWTApl` | DPM WT Applied Amount | Num | 19.6 | - |  |  |
| 84 | `DpmWTAplSC` | DPM WT Applied Amount (SC) | Num | 19.6 | - |  |  |
| 85 | `DpmWTAplFC` | DPM WT Applied Amount (FC) | Num | 19.6 | - |  |  |
| 86 | `WTTypeId` | WT Type Id | Int | 11 | [OWTT](OWTT.md) |  |  |
| 87 | `LnBsAmt` | BR Line WT Base Amount | Num | 19.6 | - |  |  |
| 88 | `LnBsAmtSC` | BR Line WT Base Amount(SC) | Num | 19.6 | - |  |  |
| 89 | `LnBsAmtFC` | BR Line WT Base Amount(FC) | Num | 19.6 | - |  |  |
| 90 | `LnCmTAmt` | BR Line Cumulated Taxable Amount | Num | 19.6 | - |  |  |
| 91 | `LnCmTAmtSC` | BR Line Cumulated Taxable Amount(SC) | Num | 19.6 | - |  |  |
| 92 | `LnCmTAmtFC` | BR Line Cumulated Taxable Amount(FC) | Num | 19.6 | - |  |  |
| 93 | `TDSType` | TDS Type | VarChar | 1 | - |  | `E` = eTDS<br>`D` = GST TDS<br>`C` = GST TCS<br>`S` = SALES TCS |
| 94 | `IgstAcc` | IGST Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 95 | `CgstAcc` | CGST Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 96 | `SgstAcc` | SGST Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 97 | `IgstAmnt` | IGST Tax Amount | Num | 19.6 | - |  |  |
| 98 | `IgstAmntSC` | IGST Tax Amount (SC) | Num | 19.6 | - |  |  |
| 99 | `IgstAmntFC` | IGST Tax Amount (FC) | Num | 19.6 | - |  |  |
| 100 | `CgstAmnt` | CGST Tax Amount | Num | 19.6 | - |  |  |
| 101 | `CgstAmntSC` | CGST Tax Amount (SC) | Num | 19.6 | - |  |  |
| 102 | `CgstAmntFC` | CGST Tax Amount (FC) | Num | 19.6 | - |  |  |
| 103 | `SgstAmnt` | SGST Tax Amount | Num | 19.6 | - |  |  |
| 104 | `SgstAmntSC` | SGST Tax Amount (SC) | Num | 19.6 | - |  |  |
| 105 | `SgstAmntFC` | SGST Tax Amount (FC) | Num | 19.6 | - |  |  |
| 106 | `IgstRate` | IGST Rate | Num | 19.6 | - |  |  |
| 107 | `CgstRate` | CGST Rate | Num | 19.6 | - |  |  |
| 108 | `SgstRate` | SGST Rate | Num | 19.6 | - |  |  |
| 109 | `IgstBAmt` | IGST Base Amount | Num | 19.6 | - |  |  |
| 110 | `IgstBAmtSC` | IGST Base Amount (SC) | Num | 19.6 | - |  |  |
| 111 | `IgstBAmtFC` | IGST Base Amount (FC) | Num | 19.6 | - |  |  |
| 112 | `CgstBAmt` | CGST Base Amount | Num | 19.6 | - |  |  |
| 113 | `CgstBAmtSC` | CGST Base Amount (SC) | Num | 19.6 | - |  |  |
| 114 | `CgstBAmtFC` | CGST Base Amount (FC) | Num | 19.6 | - |  |  |
| 115 | `SgstBAmt` | SGST Base Amount | Num | 19.6 | - |  |  |
| 116 | `SgstBAmtSC` | SGST Base Amount (SC) | Num | 19.6 | - |  |  |
| 117 | `SgstBAmtFC` | SGST Base Amount (FC) | Num | 19.6 | - |  |  |
| 118 | `IgstAppl` | Applied IGST Amount | Num | 19.6 | - |  |  |
| 119 | `IgstApplSC` | Applied IGST Amount (SC) | Num | 19.6 | - |  |  |
| 120 | `IgstApplFC` | Applied IGST Amount (FC) | Num | 19.6 | - |  |  |
| 121 | `CgstAppl` | Applied CGST Amount | Num | 19.6 | - |  |  |
| 122 | `CgstApplSC` | Applied CGST Amount (SC) | Num | 19.6 | - |  |  |
| 123 | `CgstApplFC` | Applied CGST Amount (FC) | Num | 19.6 | - |  |  |
| 124 | `SgstAppl` | Applied SGST Amount | Num | 19.6 | - |  |  |
| 125 | `SgstApplSC` | Applied SGST Amount (SC) | Num | 19.6 | - |  |  |
| 126 | `SgstApplFC` | Applied SGST Amount (FC) | Num | 19.6 | - |  |  |
| 127 | `UtgstAcc` | UTGST Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 128 | `CsgstAcc` | Cess GST Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 129 | `UtgstAmt` | UTGST Tax Amount | Num | 19.6 | - |  |  |
| 130 | `UtgstAmtSC` | UTGST Tax Amount (SC) | Num | 19.6 | - |  |  |
| 131 | `UtgstAmtFC` | UTGST Tax Amount (FC) | Num | 19.6 | - |  |  |
| 132 | `CsgstAmt` | Cess GST Tax Amount | Num | 19.6 | - |  |  |
| 133 | `CsgstAmtSC` | Cess GST Tax Amount (SC) | Num | 19.6 | - |  |  |
| 134 | `CsgstAmtFC` | Cess GST Tax Amount (FC) | Num | 19.6 | - |  |  |
| 135 | `UtgstRate` | UTGST Rate | Num | 19.6 | - |  |  |
| 136 | `CsgstRate` | Cess GST Rate | Num | 19.6 | - |  |  |
| 137 | `UtgstBAmt` | UTGST Base Amount | Num | 19.6 | - |  |  |
| 138 | `UtgstBAmtS` | UTGST Base Amount (SC) | Num | 19.6 | - |  |  |
| 139 | `UtgstBAmtF` | UTGST Base Amount (FC) | Num | 19.6 | - |  |  |
| 140 | `CsgstBAmt` | Cess GST Base Amount | Num | 19.6 | - |  |  |
| 141 | `CsgstBAmtS` | Cess GST Base Amount (SC) | Num | 19.6 | - |  |  |
| 142 | `CsgstBAmtF` | Cess GST Base Amount (FC) | Num | 19.6 | - |  |  |
| 143 | `UtgstAppl` | Applied UTGST Amount | Num | 19.6 | - |  |  |
| 144 | `UtgstApplS` | Applied UTGST Amount (SC) | Num | 19.6 | - |  |  |
| 145 | `UtgstApplF` | Applied UTGST Amount (FC) | Num | 19.6 | - |  |  |
| 146 | `CsgstAppl` | Applied Cess GST Amount | Num | 19.6 | - |  |  |
| 147 | `CsgstApplS` | Applied Cess GST Amount (SC) | Num | 19.6 | - |  |  |
| 148 | `CsgstApplF` | Applied Cess GST Amount (FC) | Num | 19.6 | - |  |  |
| 149 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 150 | `TcsIntAcct` | TCS Interim Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 151 | `SurIntAcct` | Surcharge Interim Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 152 | `CesIntAcct` | Cess Interim Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 153 | `HscIntAcct` | HSC interim Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 154 | `LnIntAcct` | Interim Account for Tax | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 155 | `FixedAmnt` | Fixed Amount | Num | 19.6 | - |  |  |
| 156 | `FixedAmtSC` | Fixed Amount (SC) | Num | 19.6 | - |  |  |
| 157 | `FixedAmtFC` | Fixed Amount (FC) | Num | 19.6 | - |  |  |
| 158 | `BaseQty` | Base Quantity | Num | 19.6 | - |  |  |
| 159 | `Accumu` | Accumulation | VarChar | 1 | - | D |  |
| 160 | `RdtParam1` | Reduction Calculation Parameter 1 | Num | 19.6 | - |  |  |
| 161 | `RdtParam2` | Reduction Calculation Parameter 2 | Num | 19.6 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineNum |
| SECONDERY | Yes | AbsEntry, WTCode, BaseAbsEnt, Doc1LineNo |
