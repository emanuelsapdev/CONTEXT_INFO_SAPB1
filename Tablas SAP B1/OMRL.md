# OMRL - Advanced Inventory Revaluation

- **Tabla:** OMRL
- **Descripción:** Advanced Inventory Revaluation
- **Cantidad de campos:** 32
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OMRL.html

## Campos (32)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `DocNum` | Document Number | Int | 11 | - |  |  |
| 3 | `Series` | Series | Int | 11 | - | 0 |  |
| 4 | `DocDate` | Posting Date | Date | 8 | - |  |  |
| 5 | `RevalType` | Inventory Valuation Type | VarChar | 1 | - | P | `P` = Price Change<br>`M` = Inventory Debit/Credit |
| 6 | `Handwrtten` | Manual Numbering | VarChar | 1 | - | N |  |
| 7 | `Printed` | Printed | VarChar | 1 | - | N | `Y` = Copy<br>`N` = Original |
| 8 | `Transfered` | Year Transfer | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 9 | `DocCur` | Document Currency | nVarChar | 3 | - |  |  |
| 10 | `DocRate` | Document Rate | Num | 19.6 | - |  |  |
| 11 | `Ref2` | Reference 2 | nVarChar | 11 | - |  |  |
| 12 | `Comments` | Remarks | nVarChar | 254 | - |  |  |
| 13 | `JrnlMemo` | Journal Remarks | nVarChar | 50 | - |  |  |
| 14 | `TransId` | Transaction Number | Int | 11 | [OJDT](OJDT.md) |  |  |
| 15 | `DocTime` | Generation Time | Int | 6 | - |  |  |
| 16 | `Confirmed` | Confirmed | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 17 | `Instance` | Instance | Int | 6 | - | 0 |  |
| 18 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 19 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 20 | `TaxDate` | Document Date | Date | 8 | - |  |  |
| 21 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Upgrade<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 22 | `StampNum` | Stamp No. | nVarChar | 16 | - |  |  |
| 23 | `FinncPriod` | Posting Period | Int | 11 | [OFPR](OFPR.md) |  |  |
| 24 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 25 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 26 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 27 | `StationID` | Workstation ID | Int | 11 | [CSTN](CSTN.md) |  |  |
| 28 | `Rounding` | Rounding | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 29 | `Segment` | Segment | Int | 6 | - | 0 |  |
| 30 | `ReqDate` | Required Date | Date | 8 | - |  |  |
| 31 | `CancelDate` | Cancelation Date | Date | 8 | - |  |  |
| 32 | `Project` | Project Code | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry |
| NUM | Yes | DocNum, Instance, Segment |
| SERIES | No | Series |
