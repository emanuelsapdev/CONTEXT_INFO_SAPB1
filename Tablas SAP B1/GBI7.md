# GBI7 - GBI Row 7 - Accounting Vouchers

- **Tabla:** GBI7
- **Descripción:** GBI Row 7 - Accounting Vouchers
- **Cantidad de campos:** 29
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/GBI7.html

## Campos (29)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `HistoryId` | History Key | Int | 11 | [OGBI](OGBI.md) |  |  |
| 2 | `RowId` | Row Number | Int | 11 | - |  |  |
| 3 | `DocDate` | Document Date | nVarChar | 8 | - |  |  |
| 4 | `DocType` | Document Type | nVarChar | 12 | - |  |  |
| 5 | `JrnEntryNo` | Journal Entry Number | nVarChar | 20 | - |  |  |
| 6 | `LnNo` | Line Number | Int | 11 | - |  |  |
| 7 | `Remark` | Details of Each Line | nVarChar | 50 | - |  |  |
| 8 | `AcctNo` | G/L Account Number | nVarChar | 15 | - |  |  |
| 9 | `Currency` | Transaction Currency | nVarChar | 3 | - |  |  |
| 10 | `Debit` | Debit Amount | Num | 19.6 | - |  |  |
| 11 | `Credit` | Credit Amount | Num | 19.6 | - |  |  |
| 12 | `FCDebit` | Debit Foreign Currency Amount | Num | 19.6 | - |  |  |
| 13 | `FCCredit` | Credit Foreign Currency Amount | Num | 19.6 | - |  |  |
| 14 | `Rate` | Exchange Rate | Num | 19.6 | - |  |  |
| 15 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 16 | `UnitPrice` | Unit Price | Num | 19.6 | - |  |  |
| 17 | `EvaGrp` | Evaluation Group | nVarChar | 254 | - |  |  |
| 18 | `SettMeth` | Settlement Method | nVarChar | 20 | - |  |  |
| 19 | `BillType` | Bill Type | nVarChar | 20 | - |  |  |
| 20 | `BillNo` | Bill Number | nVarChar | 30 | - |  |  |
| 21 | `BillDate` | Bill Date | nVarChar | 8 | - |  |  |
| 22 | `AttmtNum` | Number of Attachments | Int | 6 | - |  |  |
| 23 | `Creator` | Creator of the Voucher | nVarChar | 155 | - |  |  |
| 24 | `Approver` | Approver of the Voucher | nVarChar | 155 | - |  |  |
| 25 | `Bookkeeper` | Bookkeeper | nVarChar | 155 | - |  |  |
| 26 | `Cashier` | Cashier | nVarChar | 155 | - |  |  |
| 27 | `Posted` | Posted Sign | VarChar | 1 | - | 1 | `1`<br>`0` |
| 28 | `Reversed` | Reversed Sign | VarChar | 1 | - | 0 | `1`<br>`0` |
| 29 | `DocNum` | Document Number | nVarChar | 20 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | HistoryId, RowId |
