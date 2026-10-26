# PQT27 - Purchase Quotation - E-Books(GR) Rows

- **Tabla:** PQT27
- **Descripción:** Purchase Quotation - E-Books(GR) Rows
- **Cantidad de campos:** 33
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/PQT27.html

## Campos (33)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | [OPQT](OPQT.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `RelateType` | Relation Type | Int | 11 | - | -1 | `1` = Row<br>`2` = Row Expenses<br>`3` = Document Expenses<br>`13` = Distributed Freights<br>`-1` = Manual |
| 4 | `RelateLine` | Relation Row Number | Int | 11 | - | -1 |  |
| 5 | `GroupNum` | Group Number | Int | 11 | - | -1 |  |
| 6 | `LineTotal` | Line Total | Num | 19.6 | - |  |  |
| 7 | `LineTotalF` | Line Total (FC) | Num | 19.6 | - |  |  |
| 8 | `LineTotalS` | Line Total (SC) | Num | 19.6 | - |  |  |
| 9 | `InClassTyp` | Income Classification Type | Int | 11 | [OICP](OICP.md) |  |  |
| 10 | `InClassCat` | Income Classification Category | Int | 11 | [OICC](OICC.md) |  |  |
| 11 | `ExClassTyp` | Expense Classification Type | Int | 11 | [OECP](OECP.md) |  |  |
| 12 | `ExClassCat` | Expense Classification Cat. | Int | 11 | [OECC](OECC.md) |  |  |
| 13 | `VatCate` | VAT Category | Int | 11 | - |  |  |
| 14 | `NetValue` | Net Value | Num | 19.6 | - |  |  |
| 15 | `NetValueFC` | Net Value (FC) | Num | 19.6 | - |  |  |
| 16 | `NetValueSC` | Net Value (SC) | Num | 19.6 | - |  |  |
| 17 | `VatAmount` | VAT Amount | Num | 19.6 | - |  |  |
| 18 | `VatAmFC` | VAT Amount (FC) | Num | 19.6 | - |  |  |
| 19 | `VatAmSC` | VAT Amount (SC) | Num | 19.6 | - |  |  |
| 20 | `WtPercCat` | Withheld Percentage Category | Int | 11 | - |  |  |
| 21 | `WtAmount` | Withheld Amount | Num | 19.6 | - |  |  |
| 22 | `WtAmountFC` | Withheld Amount (FC) | Num | 19.6 | - |  |  |
| 23 | `WtAmountSC` | Withheld Amount (SC) | Num | 19.6 | - |  |  |
| 24 | `ObjectType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 540000006 |  |
| 25 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 26 | `WtCategory` | Withheld Category | VarChar | 1 | - |  | `I` = Invoice<br>`P` = Payment |
| 27 | `VATClassTy` | VAT Classification Type | Int | 11 | [OECP](OECP.md) |  |  |
| 28 | `VATClassCa` | VAT Classification Category | Int | 11 | [OECC](OECC.md) |  |  |
| 29 | `EBVatExCau` | VAT Exemption Cause | Int | 11 | [OVEC](OVEC.md) |  |  |
| 30 | `RecType` | Rec Type | Int | 11 | [OREC](OREC.md) |  |  |
| 31 | `StampDutyC` | Stamp Duty Categgory | Int | 11 | [OSDC](OSDC.md) |  |  |
| 32 | `OtherTaxCt` | Other Tax Category | Int | 11 | [OEOT](OEOT.md) |  |  |
| 33 | `FeesCtegr` | Fees Category | Int | 11 | [OEFC](OEFC.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum |
| RELATE_ROW | No | DocEntry, RelateType, RelateLine, GroupNum |
