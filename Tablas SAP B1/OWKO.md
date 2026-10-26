# OWKO - Production Instructions

- **Tabla:** OWKO
- **Descripción:** Production Instructions
- **Cantidad de campos:** 31
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OWKO.html

## Campos (31)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `OrderNum` | Instruction Key | Int | 11 | - | 0 |  |
| 2 | `Status` | Processing Status | VarChar | 1 | - | O | `O` = Work Instructions<br>`I` = Work Instructions<br>`E` = Production Completed |
| 3 | `Canceled` | Order Canceled Yes/No | VarChar | 1 | - | N | `Y` = Canceled<br>`N` = Not Canceled |
| 4 | `OrderDate` | Order Date | Date | 8 | - |  |  |
| 5 | `ProdctDate` | Work Start Date | Date | 8 | - |  |  |
| 6 | `ExpFinishD` | Expected Completion Date | Date | 8 | - |  |  |
| 7 | `FinishDate` | Work Finish Date | Date | 8 | - |  |  |
| 8 | `FinishUser` | Name of Person Receiving Instructions | nVarChar | 8 | [OUSR](OUSR.md) |  |  |
| 9 | `CardCode` | Sold-to Party Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 10 | `CustomName` | Sold-to Party Name | nVarChar | 200 | - |  |  |
| 11 | `NumInCustm` | Customer Ref. No. | nVarChar | 16 | - |  |  |
| 12 | `TotalOrder` | Order Total | Num | 19.6 | - |  |  |
| 13 | `TotalCurr` | Total Currency | nVarChar | 3 | - |  |  |
| 14 | `DocTime` | Generation Time | Int | 6 | - |  |  |
| 15 | `Memo` | Remarks | nVarChar | 254 | - |  |  |
| 16 | `SerialNum` | Instruction Number | Int | 11 | - |  |  |
| 17 | `CntctCode` | Contact Person | Int | 11 | [OCPR](OCPR.md) | 0 |  |
| 18 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 19 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 20 | `Transfered` | Postponed to Next Year | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 21 | `Instance` | Instance | Int | 6 | - | 0 |  |
| 22 | `Series` | Series | Int | 11 | [NNM1](NNM1.md) |  |  |
| 23 | `ActWorkCod` | Active Account Code | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 24 | `ActWorkSum` | Work Total | Num | 19.6 | - |  |  |
| 25 | `JrnlMemo` | Journal Remarks | nVarChar | 254 | - |  |  |
| 26 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 27 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 68 |  |
| 28 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 29 | `PriceList` | Price List | Int | 6 | [OPLN](OPLN.md) | 1 |  |
| 30 | `FinncPriod` | Posting Period | Int | 11 | [OFPR](OFPR.md) |  |  |
| 31 | `SysRate` | System Rate | Num | 19.6 | - |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | OrderNum |
| SERIAL | Yes | SerialNum, Instance |
| SERIES | No | Series |
