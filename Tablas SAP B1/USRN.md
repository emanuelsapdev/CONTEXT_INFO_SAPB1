# USRN - Serial Numbers Master Data

- **Tabla:** USRN
- **Descripción:** Serial Numbers Master Data
- **Cantidad de campos:** 32
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/USRN.html

## Campos (32)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 2 | `SysNumber` | System Number | Int | 11 | - |  |  |
| 3 | `DistNumber` | Serial Number | nVarChar | 36 | - |  |  |
| 4 | `MnfSerial` | Manufacturer Serial No. | nVarChar | 36 | - |  |  |
| 5 | `LotNumber` | Lot Number | nVarChar | 36 | - |  |  |
| 6 | `ExpDate` | Expiration Date | Date | 8 | - |  |  |
| 7 | `MnfDate` | Manufacturing Date | Date | 8 | - |  |  |
| 8 | `InDate` | Admission Date | Date | 8 | - |  |  |
| 9 | `GrntStart` | Mfr Warranty Start Date | Date | 8 | - |  |  |
| 10 | `GrntExp` | Mfr Warranty End Date | Date | 8 | - |  |  |
| 11 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 12 | `Location` | Location | nVarChar | 100 | - |  |  |
| 13 | `Status` | Status | VarChar | 1 | - |  | `0` = Available<br>`1` = Unavailable<br>`2` = Allocated |
| 14 | `Notes` | Details | Text | 16 | - |  |  |
| 15 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 16 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 17 | `Transfered` | Transferred | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 18 | `Instance` | Instance | Int | 6 | - | 0 |  |
| 19 | `AbsEntry` | Abs. Entry | Int | 11 | - |  |  |
| 20 | `ObjType` | Object Type | nVarChar | 20 | - |  |  |
| 21 | `itemName` | Item Description | nVarChar | 200 | - |  |  |
| 22 | `LogInstanc` | Log Instance | Int | 11 | - |  |  |
| 23 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 24 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 25 | `CostTotal` | Total Cost of Batches | Num | 19.6 | - |  |  |
| 26 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 27 | `QuantOut` | Output Quantity | Num | 19.6 | - |  |  |
| 28 | `PriceDiff` | Price Difference | Num | 19.6 | - |  |  |
| 29 | `Balance` | Batch Balance | Num | 19.6 | - |  |  |
| 30 | `TrackingNt` | CCD Tracking Note | Int | 11 | [OTCN](OTCN.md) |  |  |
| 31 | `TrackiNtLn` | CCD Tracking Note Line | Int | 11 | [TCN1](TCN1.md) |  |  |
| 32 | `SumDec` | Totals Accuracy for SnB | Int | 6 | - |  |  |

## Claves e índices (4)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| SYSTEM_KEY | Yes | ItemCode, SysNumber |
| DIST_KEY | No | ItemCode, DistNumber |
| LOT_KEY | No | ItemCode, LotNumber |
