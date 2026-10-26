# RTW1 - Boleto Retorno Wizard: Import Table

- **Tabla:** RTW1
- **Descripción:** Boleto Retorno Wizard: Import Table
- **Cantidad de campos:** 44
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RTW1.html

## Campos (44)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `BoeMatch` | BoE Match | nVarChar | 10 | - |  |  |
| 3 | `BoeNo` | BoE Number | nVarChar | 10 | - |  |  |
| 4 | `BoeDate` | BoE Date | Date | 8 | - |  |  |
| 5 | `BoeDueDate` | BoE Due Date | Date | 8 | - |  |  |
| 6 | `CreditDate` | Credit Date | Date | 8 | - |  |  |
| 7 | `CurrBoeSt` | Current BoE Status | VarChar | 1 | - |  | `G` = Generated<br>`S` = Sent<br>`D` = Deposited<br>`P` = Paid<br>`C` = Canceled<br>`L` = Closed<br>`F` = Failed<br>`V` = BoE to Vendor |
| 8 | `ReqBoeSt` | Requested BoE Status | VarChar | 1 | - |  | `G` = Generated<br>`S` = Sent<br>`D` = Deposited<br>`P` = Paid<br>`C` = Canceled<br>`L` = Closed<br>`F` = Failed<br>`V` = BoE to Vendor |
| 9 | `Instruct1` | BoE Instruction 1 | nVarChar | 2 | - |  |  |
| 10 | `Instruct2` | BoE Instruction 2 | nVarChar | 2 | - |  |  |
| 11 | `CancelCode` | Cancellation Code | nVarChar | 4 | - |  |  |
| 12 | `MovmntCode` | Movement Code | Int | 6 | - |  |  |
| 13 | `OccurCode` | Occurrence Code | Int | 6 | - |  |  |
| 14 | `OccurDate` | Occurrence Date | Date | 8 | - |  |  |
| 15 | `Portfolio` | Portfolio | VarChar | 1 | - |  |  |
| 16 | `OurNum` | Our Number | Int | 11 | - |  |  |
| 17 | `ValueOfT` | Value of Title | Num | 19.6 | - |  |  |
| 18 | `NetAmnt` | Net Amount | Num | 19.6 | - |  |  |
| 19 | `PaidAmnt` | Paid Amount | Num | 19.6 | - |  |  |
| 20 | `FineAmnt` | Fine Amount | Num | 19.6 | - |  |  |
| 21 | `IntAmnt` | Interest Amount | Num | 19.6 | - |  |  |
| 22 | `Discounts` | Discount Amount | Num | 19.6 | - |  |  |
| 23 | `ServiceFee` | Service Fee | Num | 19.6 | - |  |  |
| 24 | `IOFTax` | IOF Tax | Num | 19.6 | - |  |  |
| 25 | `OtherCred` | Other Credits | Num | 19.6 | - |  |  |
| 26 | `OtherExp` | Other Expenses | Num | 19.6 | - |  |  |
| 27 | `OtherInc` | Other Incomes | Num | 19.6 | - |  |  |
| 28 | `Errors` | Errors | nVarChar | 8 | - |  |  |
| 29 | `RefNum` | Reference No. | nVarChar | 254 | - |  |  |
| 30 | `Ref2` | Reference 2 | nVarChar | 254 | - |  |  |
| 31 | `CardName` | BP Name | nVarChar | 200 | - |  |  |
| 32 | `BoEBPName` | BoE BP Name | nVarChar | 200 | - |  |  |
| 33 | `MatchCode` | Match Code | VarChar | 1 | - | N | `A` = Automatic<br>`M` = Manual<br>`N` = Not Identified |
| 34 | `Selected` | Selected | VarChar | 1 | - | N |  |
| 35 | `BoeRec` | BoE Record Number | Int | 11 | - |  |  |
| 36 | `RetIndex` | RET File Record Index | Int | 11 | - |  |  |
| 37 | `Filtered` | Filtered | VarChar | 1 | - | Y |  |
| 38 | `Executed` | Executed | VarChar | 1 | - | N |  |
| 39 | `Failed` | Failed | VarChar | 1 | - | N |  |
| 40 | `LastRun` | Last Run | VarChar | 1 | - | N |  |
| 41 | `ErrorMsg` | Error Message | nVarChar | 254 | - |  |  |
| 42 | `JETransId` | JE Trans. ID | nVarChar | 10 | - |  |  |
| 43 | `CardCode` | BoE BP Code | nVarChar | 15 | - |  |  |
| 44 | `PostType` | Transaction Type | VarChar | 1 | - | C | `C` = Collection<br>`D` = Discounted |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
