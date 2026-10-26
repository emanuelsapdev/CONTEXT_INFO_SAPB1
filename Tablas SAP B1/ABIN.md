# ABIN - Bin Location - History

- **Tabla:** ABIN
- **Descripción:** Bin Location - History
- **Cantidad de campos:** 64
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ABIN.html

## Campos (64)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `BinCode` | Bin Location Code | nVarChar | 228 | - |  |  |
| 3 | `WhsCode` | Warehouse Code | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 4 | `SysBin` | System Bin | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 5 | `SL1Abs` | Sublevel-1 Internal Number | Int | 11 | [OBSL](OBSL.md) |  |  |
| 6 | `SL1Code` | Sublevel-1 Code | nVarChar | 50 | - |  |  |
| 7 | `SL2Abs` | Sublevel-2 Internal Number | Int | 11 | [OBSL](OBSL.md) |  |  |
| 8 | `SL2Code` | Sublevel-2 Code | nVarChar | 50 | - |  |  |
| 9 | `SL3Abs` | Sublevel-3 Internal Number | Int | 11 | [OBSL](OBSL.md) |  |  |
| 10 | `SL3Code` | Sublevel-3 Code | nVarChar | 50 | - |  |  |
| 11 | `SL4Abs` | Sublevel-4 Internal Number | Int | 11 | [OBSL](OBSL.md) |  |  |
| 12 | `SL4Code` | Sublevel-4 Code | nVarChar | 50 | - |  |  |
| 13 | `Attr1Abs` | Attribute-1 Internal Number | Int | 11 | [OBAT](OBAT.md) |  |  |
| 14 | `Attr1Val` | Attribute-1 Value | nVarChar | 20 | - |  |  |
| 15 | `Attr2Abs` | Attribute-2 Internal Number | Int | 11 | [OBAT](OBAT.md) |  |  |
| 16 | `Attr2Val` | Attribute-2 Value | nVarChar | 20 | - |  |  |
| 17 | `Attr3Abs` | Attribute-3 Internal Number | Int | 11 | [OBAT](OBAT.md) |  |  |
| 18 | `Attr3Val` | Attribute-3 Value | nVarChar | 20 | - |  |  |
| 19 | `Attr4Abs` | Attribute-4 Internal Number | Int | 11 | [OBAT](OBAT.md) |  |  |
| 20 | `Attr4Val` | Attribute-4 Value | nVarChar | 20 | - |  |  |
| 21 | `Attr5Abs` | Attribute-5 Internal Number | Int | 11 | [OBAT](OBAT.md) |  |  |
| 22 | `Attr5Val` | Attribute-5 Value | nVarChar | 20 | - |  |  |
| 23 | `Attr6Abs` | Attribute-6 Internal Number | Int | 11 | [OBAT](OBAT.md) |  |  |
| 24 | `Attr6Val` | Attribute-6 Value | nVarChar | 20 | - |  |  |
| 25 | `Attr7Abs` | Attribute-7 Internal Number | Int | 11 | [OBAT](OBAT.md) |  |  |
| 26 | `Attr7Val` | Attribute-7 Value | nVarChar | 20 | - |  |  |
| 27 | `Attr8Abs` | Attribute-8 Internal Number | Int | 11 | [OBAT](OBAT.md) |  |  |
| 28 | `Attr8Val` | Attribute-8 Value | nVarChar | 20 | - |  |  |
| 29 | `Attr9Abs` | Attribute-9 Internal Number | Int | 11 | [OBAT](OBAT.md) |  |  |
| 30 | `Attr9Val` | Attribute-9 Value | nVarChar | 20 | - |  |  |
| 31 | `Attr10Abs` | Attribute-10 Internal Number | Int | 11 | [OBAT](OBAT.md) |  |  |
| 32 | `Attr10Val` | Attribute-10 Value | nVarChar | 20 | - |  |  |
| 33 | `Disabled` | Inactive | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 34 | `Descr` | Description | nVarChar | 50 | - |  |  |
| 35 | `BarCode` | Bar Code | nVarChar | 100 | - |  |  |
| 36 | `AltSortCod` | Alternative Sort Code | nVarChar | 50 | - |  |  |
| 37 | `ItmRtrictT` | Item Restriction Type | Int | 6 | - | 0 | `0` = None<br>`1` = Specific Item<br>`2` = Single Item Only<br>`3` = Specific Item Group<br>`4` = Single Item Group Only |
| 38 | `SpcItmCode` | Specific Item Code | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 39 | `SpcItmGrpC` | Specific Item Group Code | Int | 6 | [OITB](OITB.md) |  |  |
| 40 | `SngBatch` | Batch Restriction | VarChar | 1 | - | N | `N` = None<br>`Y` = Single Batch |
| 41 | `RtrictType` | Restricted Transactions Type | Int | 6 | - | 0 | `0` = None<br>`1` = All Transactions<br>`2` = Inbound Transactions<br>`3` = Outbound Transactions<br>`4` = All Except Inventory Transfer and Counting Transactions |
| 42 | `RtrictResn` | Reason for Restriction | nVarChar | 254 | - |  |  |
| 43 | `RtrictDate` | Last Updated On | Date | 8 | - |  |  |
| 44 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 45 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 46 | `Transfered` | Year Transfer [Y/N] | VarChar | 1 | - | N |  |
| 47 | `Instance` | Instance | Int | 6 | - | 0 |  |
| 48 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 49 | `CreateDate` | Create Date | Date | 8 | - |  |  |
| 50 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 51 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 52 | `Deleted` | Deleted | VarChar | 1 | - | N |  |
| 53 | `MinLevel` | Minimum Qty | Num | 19.6 | - |  |  |
| 54 | `MaxLevel` | Maximum Qty | Num | 19.6 | - |  |  |
| 55 | `ReceiveBin` | Receiving Bin Location | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 56 | `NoAutoAllc` | Excl. fr. Auto Alloc. on Issue | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 57 | `MaxWeight1` | Maximum Weight 1 | Num | 19.6 | - |  |  |
| 58 | `Wght1Unit` | Unit of Maximum Weight 1 | Int | 6 | [OWGT](OWGT.md) |  |  |
| 59 | `MaxWeight2` | Maximum Weight 2 | Num | 19.6 | - |  |  |
| 60 | `Wght2Unit` | Unit of Maximum Weight 2 | Int | 6 | [OWGT](OWGT.md) |  |  |
| 61 | `UoMRtrict` | UoM Restriction | Int | 6 | - | 0 | `0` = None<br>`1` = Specific UoM<br>`2` = Single UoM Only<br>`3` = Specific UoM Group<br>`4` = Single UoM Group Only |
| 62 | `SpcUoMCode` | Specified UoM Code | Int | 11 | [OUOM](OUOM.md) |  |  |
| 63 | `SpcUGPCode` | Specified UoM Group Code | Int | 11 | [OUGP](OUGP.md) |  |  |
| 64 | `SngUoMCode` | Single UoM Code | Int | 11 | [OUOM](OUOM.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LogInstanc |
