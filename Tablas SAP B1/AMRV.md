# AMRV - Inventory Revaluation - History

- **Tabla:** AMRV
- **Descripción:** Inventory Revaluation - History
- **Cantidad de campos:** 32
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AMRV.html

## Campos (32)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `DocNum` | Document Number | Int | 11 | - |  |  |
| 3 | `DocDate` | Posting Date | Date | 8 | - |  |  |
| 4 | `Ref1` | Reference 1 | nVarChar | 11 | - |  |  |
| 5 | `Ref2` | Reference 2 | nVarChar | 11 | - |  |  |
| 6 | `Comments` | Remarks | nVarChar | 254 | - |  |  |
| 7 | `JrnlMemo` | Journal Remarks | nVarChar | 254 | - |  |  |
| 8 | `TransId` | Transaction Number | Int | 11 | [OJDT](OJDT.md) |  |  |
| 9 | `DocTime` | Generation Time | Int | 6 | - |  |  |
| 10 | `RevalType` | Inventory Revaluation Type | VarChar | 1 | - | P | `P` = Price Change<br>`M` = Material Debit/Credit |
| 11 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 12 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 13 | `Series` | Series | Int | 11 | [NNM1](NNM1.md) | 0 |  |
| 14 | `TaxDate` | Document Date | Date | 8 | - |  |  |
| 15 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Upgrade<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Auto. Incr.<br>`D` = Data Document<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 16 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 17 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 18 | `StationID` | Workstation ID | Int | 11 | [CSTN](CSTN.md) |  |  |
| 19 | `RIncmAcct` | Invent. Reval. Expense Account | nVarChar | 15 | - |  |  |
| 20 | `RExpnAcct` | Invent. Reval. Expense Account | nVarChar | 15 | - |  |  |
| 21 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 22 | `ObjType` | Object Type | nVarChar | 20 | - | 162 |  |
| 23 | `SeqCode` | Sequence Code | Int | 6 | - |  |  |
| 24 | `Serial` | Serial Number | Int | 11 | - |  |  |
| 25 | `SeriesStr` | Series String | nVarChar | 3 | - |  |  |
| 26 | `SubStr` | Subseries String | nVarChar | 3 | - |  |  |
| 27 | `VersionNum` | Version Number | nVarChar | 13 | - |  |  |
| 28 | `InflaReval` | Inflation-Based Revaluation | VarChar | 1 | - | N |  |
| 29 | `SupplCode` | Supplementary Code | nVarChar | 254 | - |  |  |
| 30 | `CardCode` | Customer/Vendor Code | nVarChar | 15 | - |  |  |
| 31 | `CardName` | Customer/Vendor Name | nVarChar | 200 | - |  |  |
| 32 | `CreatedBy` | Entry Creation Origin | VarChar | 1 | - | M | `M` = Created Manually by User<br>`W` = Created by Production Cost Recalculation Wizard |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LogInstanc, ObjType |
| NUM | No | DocNum, LogInstanc, ObjType |
| SERIES | No | Series |
