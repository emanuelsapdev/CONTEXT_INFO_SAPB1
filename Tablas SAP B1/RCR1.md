# RCR1 - Recurring Postings - Rows

- **Tabla:** RCR1
- **Descripción:** Recurring Postings - Rows
- **Cantidad de campos:** 29
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RCR1.html

## Campos (29)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `RcurCode` | Recurring Postings Code | nVarChar | 8 | [ORCR](ORCR.md) |  |  |
| 2 | `LineId` | Row Number | Int | 11 | - | 0 |  |
| 3 | `AcctCode` | Account Code | nVarChar | 15 | - |  |  |
| 4 | `AcctDesc` | Account Description | nVarChar | 200 | - |  |  |
| 5 | `Debit` | Debit | Num | 19.6 | - |  |  |
| 6 | `Credit` | Credit | Num | 19.6 | - |  |  |
| 7 | `Currency` | Currency | nVarChar | 3 | - |  |  |
| 8 | `Instance` | Instance | Int | 6 | - |  |  |
| 9 | `VatGroup` | Tax Group | nVarChar | 8 | [OVTG](OVTG.md) |  |  |
| 10 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 11 | `VatLine` | VAT Row | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 12 | `CtrlAcct` | Control Account | nVarChar | 15 | - |  |  |
| 13 | `OcrCode` | Distr. Rule | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 14 | `TaxType` | Tax Type | Int | 6 | - | 0 |  |
| 15 | `TaxPostAcc` | Tax Posting Account | VarChar | 1 | - | N | `N`<br>`R` = Sales Tax Account<br>`P` = Purchasing Tax Account |
| 16 | `StaCode` | Authority Code | nVarChar | 8 | [OSTA](OSTA.md) |  |  |
| 17 | `StaType` | Authority Type | Int | 11 | [OSTT](OSTT.md) |  |  |
| 18 | `TaxCode` | Tax Code | nVarChar | 8 | [OSTC](OSTC.md) |  |  |
| 19 | `OcrCode1` | Costing Code 1 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 20 | `OcrCode2` | Costing Code 2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 21 | `OcrCode3` | Costing Code 3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 22 | `OcrCode4` | Costing Code 4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 23 | `OcrCode5` | Costing Code 5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 24 | `WtLiable` | WTax-Liable | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 25 | `WTaxLine` | WTax Row | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 26 | `GrossValue` | Gross Value | Num | 19.6 | - |  |  |
| 27 | `Project` | Project Code | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 28 | `BPLId` | Branch | Int | 11 | [OBPL](OBPL.md) |  |  |
| 29 | `CemCode` | Cost Element Code | nVarChar | 20 | [OCEM](OCEM.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | RcurCode, Instance, LineId |
