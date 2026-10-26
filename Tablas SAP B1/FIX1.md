# FIX1 - Fixed Asset Transaction - Rows

- **Tabla:** FIX1
- **Descripción:** Fixed Asset Transaction - Rows
- **Cantidad de campos:** 34
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/FIX1.html

## Campos (34)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [OFIX](OFIX.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `ItemCode` | Item Code | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 4 | `DprArea` | Depreciation Area ID | nVarChar | 15 | [ODPA](ODPA.md) |  |  |
| 5 | `PeriodCat` | Period Category ID | nVarChar | 10 | - |  |  |
| 6 | `PostPeriod` | Posting Subperiod | Int | 11 | - |  |  |
| 7 | `RefDate` | Posting Date | Date | 8 | - |  |  |
| 8 | `APC` | APC | Num | 19.6 | - |  |  |
| 9 | `OrdDpr` | Ordinary Depreciation | Num | 19.6 | - |  |  |
| 10 | `UnpDpr` | Unplanned Depreciation | Num | 19.6 | - |  |  |
| 11 | `SpDprKey1` | Special Depreciation Key 01 | nVarChar | 2 | [ODPP](ODPP.md) |  |  |
| 12 | `SpDpr1` | Special Depreciation 01 | Num | 19.6 | - |  |  |
| 13 | `Qty` | Quantity | Num | 19.6 | - |  |  |
| 14 | `DprType` | New Depreciation Type | nVarChar | 15 | [ODTP](ODTP.md) |  |  |
| 15 | `DprDate` | New Depreciation Start Date | Date | 8 | - |  |  |
| 16 | `RemLife` | New Remaining Life | Int | 11 | - |  |  |
| 17 | `SalvageVal` | New Salvage Value | Num | 19.6 | - |  |  |
| 18 | `RecvAsst` | Receiving Item Code | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 19 | `RetirDate` | Retirement Date | Date | 8 | - |  |  |
| 20 | `SpDprKey2` | Special Depreciation Key 02 | nVarChar | 2 | [ODPP](ODPP.md) |  |  |
| 21 | `SpDpr2` | Special Depreciation 02 | Num | 19.6 | - |  |  |
| 22 | `SpDprKey3` | Special Depreciation Key 03 | nVarChar | 2 | [ODPP](ODPP.md) |  |  |
| 23 | `TransType` | Transaction Type | nVarChar | 4 | - |  | `0` = Unknown<br>`110` = Acquisition<br>`115` = Subacquisition<br>`120` = Credit Memo<br>`210` = Full Retirement<br>`220` = Full Scrapping<br>`230` = Partial Retirement<br>`240` = Partial Scrapping<br>`260` = Low Value Asset Full Retirement<br>`270` = Low Value Asset Full Scrapping<br>`310` = Full Transfer<br>`320` = Partial Transfer<br>`330` = Asset Class Transfer<br>`410` = Manual Ordinary Depreciation<br>`420` = Manual Unplanned Depreciation<br>`430` = Manual Special Depreciation<br>`440` = Appreciation<br>`550` = Revaluation<br>`510` = Change of Depreciation Type<br>`520` = Change of Useful Life<br>`530` = Change of Depreciation Start Date<br>`540` = Change of Salvage Value<br>`560` = Change of Period Control<br>`570` = Change of Total Units |
| 24 | `UsefulLife` | New Useful Life | Int | 11 | - |  |  |
| 25 | `Appr` | Appreciation | Num | 19.6 | - |  |  |
| 26 | `WriteUp` | Write-Up | Num | 19.6 | - |  |  |
| 27 | `DeltaDays` | Delta Remaining Life in Days | Int | 11 | - |  |  |
| 28 | `NewAstCls` | New Asset Class | nVarChar | 20 | [OACS](OACS.md) |  |  |
| 29 | `HistOrdDpr` | Historical Ordinary Depr. | Num | 19.6 | - |  |  |
| 30 | `SpDpr3` | Special Depreciation 03 | Num | 19.6 | - |  |  |
| 31 | `TransAmnt` | Transaction Amount | Num | 19.6 | - |  |  |
| 32 | `Remark` | Remarks | nVarChar | 254 | - |  |  |
| 33 | `ReTranType` | Receiving Transaction Type | nVarChar | 4 | - | 0 | `0` = Unknown<br>`110` = Acquisition<br>`115` = Subacquisition |
| 34 | `NewTtlUnit` | New Total Unit | Int | 11 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineNum |
| SECONDARY | No | DprArea, PeriodCat, ItemCode |
