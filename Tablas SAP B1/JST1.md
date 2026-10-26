# JST1 - TDS Adjustment - Rows

- **Tabla:** JST1
- **Descripción:** TDS Adjustment - Rows
- **Cantidad de campos:** 52
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/JST1.html

## Campos (52)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Internal Number | Int | 11 | [OJST](OJST.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - | 0 |  |
| 3 | `WTCode` | WTax Code | nVarChar | 4 | [OWHT](OWHT.md) |  |  |
| 4 | `BaseNum` | Base Document Type | Int | 11 | - | -1 | `-1`<br>`18` = A/P Invoice<br>`204` = A/P Down Payment |
| 5 | `BaseAbsId` | Base Document Internal ID | Int | 11 | - |  |  |
| 6 | `BaseLine` | Base Row | Int | 11 | - |  |  |
| 7 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 8 | `Rate` | Rate | Num | 19.6 | - |  |  |
| 9 | `TdsRate` | TDS Rate | Num | 19.6 | - |  |  |
| 10 | `SurRate` | Surcharge Rate | Num | 19.6 | - |  |  |
| 11 | `CessRate` | Cess Rate | Num | 19.6 | - |  |  |
| 12 | `HscRate` | HSC Rate | Num | 19.6 | - |  |  |
| 13 | `TaxbleAmnt` | Taxable Amount | Num | 19.6 | - |  |  |
| 14 | `TxblAmntSC` | Taxable Amount (SC) | Num | 19.6 | - |  |  |
| 15 | `TxblAmntFC` | Taxable Amount (FC) | Num | 19.6 | - |  |  |
| 16 | `Category` | Category | VarChar | 1 | - |  | `P` = Payment<br>`I` = Invoice |
| 17 | `Criteria` | Criteria | VarChar | 1 | - |  | `Y` = Accrual<br>`N` = Cash |
| 18 | `Type` | Withholding Tax Type | VarChar | 1 | - |  | `V` = VAT Withholding<br>`I` = Incoming Tax Withholding |
| 19 | `RoundType` | Rounding Type | VarChar | 1 | - |  | `T` = Truncated<br>`C` = Commercial Values |
| 20 | `BaseType` | Base Type | VarChar | 1 | - |  | `G` = Gross<br>`N` = Net<br>`V` = VAT |
| 21 | `Account` | G/L Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 22 | `TdsAcc` | TDS Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 23 | `SurAcc` | Surcharge Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 24 | `CessAcc` | Cess Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 25 | `HscAcc` | HSC Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 26 | `WTAmnt` | WTax Amount | Num | 19.6 | - |  |  |
| 27 | `WTAmntSC` | WTax Amount (SC) | Num | 19.6 | - |  |  |
| 28 | `WTAmntFC` | WTax Amount (FC) | Num | 19.6 | - |  |  |
| 29 | `TdsBAmt` | TDS Base Amount | Num | 19.6 | - |  |  |
| 30 | `TdsBAmtSC` | TDS Base Amount (SC) | Num | 19.6 | - |  |  |
| 31 | `TdsBAmtFC` | TDS Base Amount (FC) | Num | 19.6 | - |  |  |
| 32 | `SurBAmt` | Surcharge Base Amount | Num | 19.6 | - |  |  |
| 33 | `SurBAmtSC` | Surcharge Base Amount (SC) | Num | 19.6 | - |  |  |
| 34 | `SurBAmtFC` | Surcharge Base Amount (FC) | Num | 19.6 | - |  |  |
| 35 | `CessBAmt` | Cess Base Amount | Num | 19.6 | - |  |  |
| 36 | `CessBAmtSC` | Cess Base Amount (SC) | Num | 19.6 | - |  |  |
| 37 | `CessBAmtFC` | Cess Base Amount (FC) | Num | 19.6 | - |  |  |
| 38 | `HscBAmt` | HSC Base Amount | Num | 19.6 | - |  |  |
| 39 | `HscBAmtSC` | HSC Base Amount (SC) | Num | 19.6 | - |  |  |
| 40 | `HscBAmtFC` | HSC Base Amount (FC) | Num | 19.6 | - |  |  |
| 41 | `TdsAmnt` | TDS Tax Amount | Num | 19.6 | - |  |  |
| 42 | `TdsAmntSC` | TDS Tax Amount (SC) | Num | 19.6 | - |  |  |
| 43 | `TdsAmntFC` | TDS Tax Amount (FC) | Num | 19.6 | - |  |  |
| 44 | `SurAmnt` | Surcharge Tax Amount | Num | 19.6 | - |  |  |
| 45 | `SurAmntSC` | Surcharge Tax Amount (SC) | Num | 19.6 | - |  |  |
| 46 | `SurAmntFC` | Surcharge Tax Amount (FC) | Num | 19.6 | - |  |  |
| 47 | `CessAmnt` | Cess Tax Amount | Num | 19.6 | - |  |  |
| 48 | `CessAmntSC` | Cess Tax Amount (SC) | Num | 19.6 | - |  |  |
| 49 | `CessAmntFC` | Cess Tax Amount (FC) | Num | 19.6 | - |  |  |
| 50 | `HscAmnt` | HSC Tax Amount | Num | 19.6 | - |  |  |
| 51 | `HscAmntSC` | HSC Tax Amount (SC) | Num | 19.6 | - |  |  |
| 52 | `HscAmntFC` | HSC Tax Amount (FC) | Num | 19.6 | - |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId, LineNum |
| BASE_ENTRY | No | AbsId, BaseNum, BaseAbsId, BaseLine |
| WT_CODE | No | AbsId, WTCode |
