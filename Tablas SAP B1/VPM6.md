# VPM6 - Outgoing Payments - WTax Rows

- **Tabla:** VPM6
- **Descripción:** Outgoing Payments - WTax Rows
- **Cantidad de campos:** 78
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/VPM6.html

## Campos (78)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocNum` | Document Number | Int | 11 | [OVPM](OVPM.md) |  |  |
| 2 | `InvoiceId` | Invoice Key | Int | 11 | - |  |  |
| 3 | `WTCode` | WTax Code | nVarChar | 4 | [OWHT](OWHT.md) |  |  |
| 4 | `PymMean` | Payment Means | VarChar | 1 | - | C | `C` = Cash<br>`K` = Checks<br>`R` = Credit Card<br>`T` = Bank Transfer<br>`B` = Bill of Exchange |
| 5 | `DueDate` | Due Date | Date | 8 | - |  |  |
| 6 | `WTSum` | WTax Amount | Num | 19.6 | - |  |  |
| 7 | `WTSumFC` | WTax Amount (SC) | Num | 19.6 | - |  |  |
| 8 | `WTSumSC` | WTax Amount (FC) | Num | 19.6 | - |  |  |
| 9 | `Rate` | Rate | Num | 19.6 | - |  |  |
| 10 | `TaxbleAmnt` | Taxable Amount | Num | 19.6 | - |  |  |
| 11 | `TxblAmntFC` | Taxable Amount (FC) | Num | 19.6 | - |  |  |
| 12 | `TxblAmntSC` | Taxable Amount (SC) | Num | 19.6 | - |  |  |
| 13 | `PymAmount` | Payment Amount | Num | 19.6 | - |  |  |
| 14 | `PymAmounF` | Payment Amount (FC) | Num | 19.6 | - |  |  |
| 15 | `PymAmounS` | Payment Amount (SC) | Num | 19.6 | - |  |  |
| 16 | `Line` | Internal Number | Int | 11 | - |  |  |
| 17 | `LogInstanc` | Log Instance - History | Int | 11 | - | 0 |  |
| 18 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 46 |  |
| 19 | `TdsBAmt` | TDS Base Amount | Num | 19.6 | - |  |  |
| 20 | `TdsBAmtSC` | TDS Base Amount (SC) | Num | 19.6 | - |  |  |
| 21 | `TdsBAmtFC` | TDS Base Amount (FC) | Num | 19.6 | - |  |  |
| 22 | `SurBAmt` | Surcharge Base Amount | Num | 19.6 | - |  |  |
| 23 | `SurBAmtSC` | Surcharge Base Amount (SC) | Num | 19.6 | - |  |  |
| 24 | `SurBAmtFC` | Surcharge Base Amount (FC) | Num | 19.6 | - |  |  |
| 25 | `CessBAmt` | Cess Base Amount | Num | 19.6 | - |  |  |
| 26 | `CessBAmtSC` | Cess Base Amount (SC) | Num | 19.6 | - |  |  |
| 27 | `CessBAmtFC` | Cess Base Amount (FC) | Num | 19.6 | - |  |  |
| 28 | `HscBAmt` | HSC Base Amount | Num | 19.6 | - |  |  |
| 29 | `HscBAmtSC` | HSC Base Amount (SC) | Num | 19.6 | - |  |  |
| 30 | `HscBAmtFC` | HSC Base Amount (FC) | Num | 19.6 | - |  |  |
| 31 | `TdsAmnt` | TDS Tax Amount | Num | 19.6 | - |  |  |
| 32 | `TdsAmntSC` | TDS Tax Amount (SC) | Num | 19.6 | - |  |  |
| 33 | `TdsAmntFC` | TDS Tax Amount (FC) | Num | 19.6 | - |  |  |
| 34 | `SurAmnt` | Surcharge Tax Amount | Num | 19.6 | - |  |  |
| 35 | `SurAmntSC` | Surcharge Tax Amount (SC) | Num | 19.6 | - |  |  |
| 36 | `SurAmntFC` | Surcharge Tax Amount (FC) | Num | 19.6 | - |  |  |
| 37 | `CessAmnt` | Cess Tax Amount | Num | 19.6 | - |  |  |
| 38 | `CessAmntSC` | Cess Tax Amount (SC) | Num | 19.6 | - |  |  |
| 39 | `CessAmntFC` | Cess Tax Amount (FC) | Num | 19.6 | - |  |  |
| 40 | `HscAmnt` | HSC Tax Amount | Num | 19.6 | - |  |  |
| 41 | `HscAmntSC` | HSC Tax Amount (SC) | Num | 19.6 | - |  |  |
| 42 | `HscAmntFC` | HSC Tax Amount (FC) | Num | 19.6 | - |  |  |
| 43 | `WTTypeId` | WT Type Id | Int | 11 | [OWTT](OWTT.md) |  |  |
| 44 | `WTPosted` | WT Posted | Num | 19.6 | - |  |  |
| 45 | `WTPostedFC` | WT Posted FC | Num | 19.6 | - |  |  |
| 46 | `WTPostedSC` | WT Posted SC | Num | 19.6 | - |  |  |
| 47 | `IgstBAmt` | IGST Base Amount | Num | 19.6 | - |  |  |
| 48 | `IgstBAmtSC` | IGST Base Amount (SC) | Num | 19.6 | - |  |  |
| 49 | `IgstBAmtFC` | IGST Base Amount (FC) | Num | 19.6 | - |  |  |
| 50 | `CgstBAmt` | CGST Base Amount | Num | 19.6 | - |  |  |
| 51 | `CgstBAmtSC` | CGST Base Amount (SC) | Num | 19.6 | - |  |  |
| 52 | `CgstBAmtFC` | CGST Base Amount (FC) | Num | 19.6 | - |  |  |
| 53 | `SgstBAmt` | SGST Base Amount | Num | 19.6 | - |  |  |
| 54 | `SgstBAmtSC` | SGST Base Amount (SC) | Num | 19.6 | - |  |  |
| 55 | `SgstBAmtFC` | SGST Base Amount (FC) | Num | 19.6 | - |  |  |
| 56 | `IgstAmnt` | IGST Tax Amount | Num | 19.6 | - |  |  |
| 57 | `IgstAmntSC` | IGST Tax Amount (SC) | Num | 19.6 | - |  |  |
| 58 | `IgstAmntFC` | IGST Tax Amount (FC) | Num | 19.6 | - |  |  |
| 59 | `CgstAmnt` | CGST Tax Amount | Num | 19.6 | - |  |  |
| 60 | `CgstAmntSC` | CGST Tax Amount (SC) | Num | 19.6 | - |  |  |
| 61 | `CgstAmntFC` | CGST Tax Amount (FC) | Num | 19.6 | - |  |  |
| 62 | `SgstAmnt` | SGST Tax Amount | Num | 19.6 | - |  |  |
| 63 | `SgstAmntSC` | SGST Tax Amount (SC) | Num | 19.6 | - |  |  |
| 64 | `SgstAmntFC` | SGST Tax Amount (FC) | Num | 19.6 | - |  |  |
| 65 | `DepositNum` | Deposit Number | Int | 11 | [OVPM](OVPM.md) |  |  |
| 66 | `UtgstBAmt` | UTGST Base Amount | Num | 19.6 | - |  |  |
| 67 | `UtgstBAmtS` | UTGST Base Amount (SC) | Num | 19.6 | - |  |  |
| 68 | `UtgstBAmtC` | UTGST Base Amount (FC) | Num | 19.6 | - |  |  |
| 69 | `CsgstBAmt` | Cess GST Base Amount | Num | 19.6 | - |  |  |
| 70 | `CsgstBAmtS` | Cess GST Base Amount (SC) | Num | 19.6 | - |  |  |
| 71 | `CsgstBAmtC` | Cess GST Base Amount (FC) | Num | 19.6 | - |  |  |
| 72 | `UtgstAmt` | UTGST Amount | Num | 19.6 | - |  |  |
| 73 | `UtgstAmtSC` | UTGST Amount (SC) | Num | 19.6 | - |  |  |
| 74 | `UtgstAmtFC` | UTGST Amount (FC) | Num | 19.6 | - |  |  |
| 75 | `CsgstAmt` | Cess GST Amount | Num | 19.6 | - |  |  |
| 76 | `CsgstAmtSC` | Cess GST Amount (SC) | Num | 19.6 | - |  |  |
| 77 | `CsgstAmtFC` | Cess GST Amount (FC) | Num | 19.6 | - |  |  |
| 78 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocNum, Line |
