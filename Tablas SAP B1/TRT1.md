# TRT1 - Posting Templates - Rows

- **Tabla:** TRT1
- **Descripción:** Posting Templates - Rows
- **Cantidad de campos:** 26
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TRT1.html

## Campos (26)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TrtCode` | Template Code | nVarChar | 8 | [OTRT](OTRT.md) |  |  |
| 2 | `Sequence` | Sequence Row No. | Int | 11 | - |  |  |
| 3 | `AcctCode` | Account Code | nVarChar | 15 | - |  |  |
| 4 | `Line_Descr` | Account Description | nVarChar | 200 | - |  |  |
| 5 | `Debit` | Debit | Num | 19.6 | - |  |  |
| 6 | `Credit` | Credit | Num | 19.6 | - |  |  |
| 7 | `VatGroup` | Tax Group | nVarChar | 8 | [OVTG](OVTG.md) |  |  |
| 8 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 9 | `VatLine` | Vat Line | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 10 | `CtrlAcct` | Control Account | nVarChar | 15 | - |  |  |
| 11 | `OcrCode` | Distr. Rule | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 12 | `TaxType` | Tax Type | Int | 6 | - | 0 |  |
| 13 | `TaxPostAcc` | Tax Posting Account | VarChar | 1 | - | N | `N`<br>`R` = Sales Tax Account<br>`P` = Purchasing Tax Account |
| 14 | `StaCode` | Authority Code | nVarChar | 8 | [OSTA](OSTA.md) |  |  |
| 15 | `StaType` | Authority Type | Int | 11 | [OSTT](OSTT.md) |  |  |
| 16 | `TaxCode` | Tax Code | nVarChar | 8 | [OSTC](OSTC.md) |  |  |
| 17 | `OcrCode1` | Costing Code 1 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 18 | `OcrCode2` | Costing Code 2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 19 | `OcrCode3` | Costing Code 3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 20 | `OcrCode4` | Costing Code 4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 21 | `OcrCode5` | Costing Code 5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 22 | `WtLiable` | WTax-Liable | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 23 | `WTaxLine` | WTax Row | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 24 | `GrossValue` | Gross Value | Num | 19.6 | - |  |  |
| 25 | `Project` | Project Code | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 26 | `CemCode` | Cost Element Code | nVarChar | 20 | [OCEM](OCEM.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TrtCode, Sequence |
