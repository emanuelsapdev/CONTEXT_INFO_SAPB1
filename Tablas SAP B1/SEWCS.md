# SEWCS - SEWCS

- **Tabla:** SEWCS
- **Descripción:** SEWCS
- **Cantidad de campos:** 42
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SEWCS.html

## Campos (42)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CompDbNam` | Company Db Name | nVarChar | 200 | - |  |  |
| 2 | `SmpTableId` | Smp Table ID | nVarChar | 3 | - |  |  |
| 3 | `COAtemplat` | COA Template | VarChar | 1 | - |  |  |
| 4 | `LocalCurr` | Local Currency | nVarChar | 3 | - |  |  |
| 5 | `SystemCurr` | System Currenct | nVarChar | 3 | - |  |  |
| 6 | `UseSegAcc` | Use Segment Accounts | VarChar | 1 | - |  |  |
| 7 | `StkValuat` | Stock Valuation | VarChar | 1 | - |  |  |
| 8 | `PricSysPWh` | Price System Per Warehouse | VarChar | 1 | - |  |  |
| 9 | `AllowRelSt` | Stock Release w/o Cost Price | VarChar | 1 | - |  |  |
| 10 | `CostPrcLst` | Gross profit Base Price Origi | VarChar | 1 | - |  |  |
| 11 | `GrossBySal` | Calculate % GP as | VarChar | 1 | - |  |  |
| 12 | `BlkNegQuan` | Block Negative Quantity | VarChar | 1 | - |  |  |
| 13 | `RoundMeth` | Rounding Method | VarChar | 1 | - |  |  |
| 14 | `RoundVAT` | Round Tax Amount in Rows | VarChar | 1 | - |  |  |
| 15 | `EnblExpns` | Manage Expenses in Documents | VarChar | 1 | - |  |  |
| 16 | `DirectRate` | Exchange Rate Posting | VarChar | 1 | - |  |  |
| 17 | `SumDec` | Decimal - Amounts | Int | 11 | - |  |  |
| 18 | `PriceDec` | Decimal - Prices | Int | 11 | - |  |  |
| 19 | `RateDec` | Decimal - Rates | Int | 11 | - |  |  |
| 20 | `QtyDec` | Decimal - Quantities | Int | 11 | - |  |  |
| 21 | `PercentDec` | Decimal - Percent | Int | 11 | - |  |  |
| 22 | `MeasureDec` | Decimal - Units | Int | 11 | - |  |  |
| 23 | `DecSep` | Decimal - Separator | VarChar | 1 | - |  |  |
| 24 | `DpmSalAct` | Sal-DownPayment Clearing Acct | nVarChar | 15 | - |  |  |
| 25 | `DfltIncom` | Sales -Revenues Account | nVarChar | 15 | - |  |  |
| 26 | `ForgnIncm` | Sales -Revenues Foreign | nVarChar | 15 | - |  |  |
| 27 | `ECIncome` | Sales -Revenue EU | nVarChar | 15 | - |  |  |
| 28 | `SHandleWT` | Sales -enable WT | VarChar | 1 | - |  |  |
| 29 | `SDfltWT` | Sales -Default WT Code | nVarChar | 4 | - |  |  |
| 30 | `NINum` | Ni No | nVarChar | 20 | - |  |  |
| 31 | `ExpireDate` | Sales - Expiration Date | Date | 8 | - |  |  |
| 32 | `CrtfcateNO` | Sales - Certificate Number | nVarChar | 20 | - |  |  |
| 33 | `SaleVatOff` | Sales - Tax Offsetting account | nVarChar | 15 | - |  |  |
| 34 | `DfltExpn` | Purchase - Expense Account | nVarChar | 15 | - |  |  |
| 35 | `ForgnExpn` | Purchase-Foreign Expense Acct | nVarChar | 15 | - |  |  |
| 36 | `ECExepnses` | Purchase - EU Expense account | nVarChar | 15 | - |  |  |
| 37 | `DpmPurAct` | Pur-DownPayment Clearing Acct | nVarChar | 15 | - |  |  |
| 38 | `ExpVarAct` | Purchase - Variance accont | nVarChar | 15 | - |  |  |
| 39 | `PHandleWT` | Purchase - WT enabled | VarChar | 1 | - |  |  |
| 40 | `PDfltWT` | Purchase - Default WT code | nVarChar | 4 | - |  |  |
| 41 | `PurcVatOff` | Pur - Tax Offsetting account | nVarChar | 15 | - |  |  |
| 42 | `ComissAct` | Gen - Credit Card Deposit fee | nVarChar | 15 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CompDbNam |
