# SLR1 - Special Ledger - Analytical Accounting Report Lines: Revenues & Expenses

- **Tabla:** SLR1
- **Descripción:** Special Ledger - Analytical Accounting Report Lines: Revenues & Expenses
- **Cantidad de campos:** 34
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SLR1.html

## Campos (34)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocID` | Document Identification Number | Int | 11 | [OSLR](OSLR.md) |  |  |
| 2 | `LineID` | Line Identification | Int | 11 | - |  |  |
| 3 | `RuleID` | Rule Identification Number | Int | 6 | [OSCR](OSCR.md) |  |  |
| 4 | `GoalNum` | Rule Goal Number | Int | 6 | - |  |  |
| 5 | `TransType` | Transaction Type Number | Int | 6 | - |  |  |
| 6 | `PrfCntVal` | Distribution Rule Code | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 7 | `PrfCntOrig` | Orig. Distribution Rule Code | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 8 | `Checked` | Selected for Processing | VarChar | 1 | - | Y | `N` = No<br>`Y` = Yes |
| 9 | `Status` | Status | VarChar | 1 | - |  |  |
| 10 | `Enabled` | Enabled for Processing | VarChar | 1 | - | Y | `N` = No<br>`Y` = Yes |
| 11 | `DebitAct` | Debit Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 12 | `CreditAct` | Credit Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 13 | `RevSides` | Revert Debit/Credit Sides | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 14 | `Src` | Source Amount | Num | 19.6 | - |  |  |
| 15 | `SrcFC` | Source Amount, Foreign Currency | Num | 19.6 | - |  |  |
| 16 | `SrcSC` | Source Amount, System Currency | Num | 19.6 | - |  |  |
| 17 | `SrcCalc` | Calculated Amount | Num | 19.6 | - |  |  |
| 18 | `SrcCalcFC` | Calculated Amount - Foreign | Num | 19.6 | - |  |  |
| 19 | `SrcCalcSC` | Calculated Amount - System | Num | 19.6 | - |  |  |
| 20 | `FinalSum` | Final Amount | Num | 19.6 | - |  |  |
| 21 | `FinalSumFC` | Final Amount (FC) | Num | 19.6 | - |  |  |
| 22 | `FinalSumSC` | Final Amount (SC) | Num | 19.6 | - |  |  |
| 23 | `Currency` | Foreign Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 24 | `MainTable` | Main Source Table | nVarChar | 20 | - |  |  |
| 25 | `PKField0` | Primary Key Field | nVarChar | 50 | - |  |  |
| 26 | `PKField1` | Primary Key Field | nVarChar | 50 | - |  |  |
| 27 | `PKField2` | Primary Key Field | nVarChar | 50 | - |  |  |
| 28 | `PKField3` | Primary Key Field | nVarChar | 50 | - |  |  |
| 29 | `PKField4` | Primary Key Field | nVarChar | 50 | - |  |  |
| 30 | `PKField5` | Primary Key Field | nVarChar | 50 | - |  |  |
| 31 | `PKField6` | Primary Key Field | nVarChar | 50 | - |  |  |
| 32 | `PKField7` | Primary Key Field | nVarChar | 50 | - |  |  |
| 33 | `PKField8` | Primary Key Field | nVarChar | 50 | - |  |  |
| 34 | `PKField9` | Primary Key Field | nVarChar | 50 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocID, LineID |
