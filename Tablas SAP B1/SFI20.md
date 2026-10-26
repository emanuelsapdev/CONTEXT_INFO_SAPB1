# SFI20 - Intrastat Expenses

- **Tabla:** SFI20
- **Descripción:** Intrastat Expenses
- **Cantidad de campos:** 20
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SFI20.html

## Campos (20)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | [OSFI](OSFI.md) |  |  |
| 2 | `ExpnsCode` | Freight Code | Int | 11 | [OEXD](OEXD.md) |  |  |
| 3 | `TotalLC` | Total | Num | 19.6 | - |  |  |
| 4 | `TotalFC` | Total (FC) | Num | 19.6 | - |  |  |
| 5 | `TotalSC` | Total (SC) | Num | 19.6 | - |  |  |
| 6 | `DistribM` | Distribution Method | VarChar | 1 | - | T | `Q` = Quantity<br>`V` = Volume<br>`W` = Weight<br>`E` = Equally<br>`T` = Row Total |
| 7 | `DrawnLC` | Drawn Total | Num | 19.6 | - |  |  |
| 8 | `DrawnFC` | Drawn Total (FC) | Num | 19.6 | - |  |  |
| 9 | `DrawnSC` | Drawn Total (SC) | Num | 19.6 | - |  |  |
| 10 | `LineNum` | Line Number | Int | 11 | - | -1 |  |
| 11 | `BaseAbsEnt` | Base Abs. Entry | Int | 11 | - | -1 |  |
| 12 | `BaseType` | Base Document Type | Int | 11 | - | -1 | `23` = Sales Quotation<br>`17` = Sales Order<br>`15` = Delivery Notes<br>`16` = Return<br>`13` = A/R Invoice<br>`203` = Down Payment Incoming<br>`204` = Down Payment Outgoing<br>`22` = Purchase Order<br>`20` = Goods Receipt PO<br>`21` = Goods Return<br>`18` = A/P Invoice<br>`540000006` = Purchase Quotation<br>`0`<br>`-1` |
| 13 | `BaseRef` | Base Document Reference | Int | 11 | - |  |  |
| 14 | `BaseLnNum` | Base Document Row No. | Int | 11 | - | -1 |  |
| 15 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 16 | `ObjectType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 254000065 |  |
| 17 | `FixCurr` | Fixation Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 18 | `AppliedLC` | Applied | Num | 19.6 | - |  |  |
| 19 | `AppliedFC` | Applied (FC) | Num | 19.6 | - |  |  |
| 20 | `AppliedSC` | Applied (SC) | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum |
