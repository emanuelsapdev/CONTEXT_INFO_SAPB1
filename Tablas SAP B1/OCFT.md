# OCFT - Cash Flow Transactions - Rows

- **Tabla:** OCFT
- **Descripción:** Cash Flow Transactions - Rows
- **Cantidad de campos:** 20
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCFT.html

## Campos (20)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CFTId` | Cash Flow Transaction ID | Int | 11 | - |  |  |
| 2 | `CFWId` | Cash Flow Line Item ID | Int | 11 | [OCFW](OCFW.md) |  |  |
| 3 | `Debit` | Debit Amount | Num | 19.6 | - |  |  |
| 4 | `Credit` | Credit Amount | Num | 19.6 | - |  |  |
| 5 | `SysCredit` | System Credit Amount | Num | 19.6 | - |  |  |
| 6 | `SysDebit` | System Debit Amount | Num | 19.6 | - |  |  |
| 7 | `FCDebit` | FC Debit Amount | Num | 19.6 | - |  |  |
| 8 | `FCCredit` | FC Credit Amount | Num | 19.6 | - |  |  |
| 9 | `FCCurrency` | Foreign Currency | nVarChar | 3 | - |  |  |
| 10 | `Account` | Account Code | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 11 | `BatchNum` | Batch No. | Int | 11 | - |  |  |
| 12 | `JDTId` | Journal Entry ID | Int | 11 | - |  |  |
| 13 | `JDTLineId` | Journal Entry Line ID | Int | 11 | - |  |  |
| 14 | `TransType` | Source Object | nVarChar | 20 | - |  | `24` = Incoming Payment<br>`46` = Vendor Payment<br>`30` = Journal Entry<br>`140` = Payment Draft<br>`29` = Journal Vouchers List<br>`25` = Deposit<br>`76` = Postdated Check Deposit<br>`182` = Bill of Exchange Transaction<br>`42` = Bank Statement<br>`157` = Payment Wizard |
| 15 | `BaseRef` | Base Reference | nVarChar | 11 | - |  |  |
| 16 | `PaymentMen` | Payment Means | nVarChar | 11 | - |  |  |
| 17 | `PaymentRef` | Payment Reference | nVarChar | 11 | - |  |  |
| 18 | `PostDate` | Posting Date | Date | 8 | - |  |  |
| 19 | `ValueDate` | Value Date | Date | 8 | - |  |  |
| 20 | `Status` | Status | VarChar | 1 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CFTId |
