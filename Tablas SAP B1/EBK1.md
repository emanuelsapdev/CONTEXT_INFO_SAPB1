# EBK1 - E-Books - Rows

- **Tabla:** EBK1
- **Descripción:** E-Books - Rows
- **Cantidad de campos:** 23
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/EBK1.html

## Campos (23)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | E-Books Abs. Entry | Int | 11 | [OEBK](OEBK.md) |  |  |
| 2 | `LineNum` | Line Number | Int | 11 | - |  |  |
| 3 | `NetValue` | Net Value | Num | 19.6 | - |  |  |
| 4 | `VatCatgory` | VAT Category | Int | 11 | - |  |  |
| 5 | `VatAmount` | VAT Amount | Num | 19.6 | - |  |  |
| 6 | `WithheldAm` | Withheld Amount | Num | 19.6 | - |  |  |
| 7 | `WhPrctCat` | Withheld Percent Category | Int | 11 | - |  |  |
| 8 | `ExClassTyp` | Expense Classification Type | Int | 11 | [OECP](OECP.md) |  |  |
| 9 | `ExClassCat` | Expense Classification Cat. | Int | 11 | [OECC](OECC.md) |  |  |
| 10 | `VATClassTy` | VAT Classification Type | Int | 11 | [OECP](OECP.md) |  |  |
| 11 | `VATClassCa` | VAT Classification Category | Int | 11 | [OECC](OECC.md) |  |  |
| 12 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 13 | `VatExmpCat` | VAT Exemption Category | Int | 11 | [OVEC](OVEC.md) |  |  |
| 14 | `RecType` | Record Type | Int | 11 | [OREC](OREC.md) |  |  |
| 15 | `StampDutyC` | Stamp Duty Category | Int | 11 | [OSDC](OSDC.md) |  |  |
| 16 | `StampDutyA` | Stamp Duty Amount | Num | 19.6 | - |  |  |
| 17 | `OtherTaxCt` | Other Taxes Category | Int | 11 | [OEOT](OEOT.md) |  |  |
| 18 | `OtherTaxAt` | Othe Taxes Amount | Num | 19.6 | - |  |  |
| 19 | `FeesCtegr` | Fees Category | Int | 11 | [OEFC](OEFC.md) |  |  |
| 20 | `FeesAmount` | Fees Amount | Num | 19.6 | - |  |  |
| 21 | `DiscOption` | Discount Option | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 22 | `LineType` | Details or Taxes | Int | 11 | - | 1 | `1` = Invoice Details<br>`2` = Taxes |
| 23 | `UnderLyAmt` | Underlying Amount | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineNum, VatCatgory |
