# ARSC - Resource Master Data - Log

- **Tabla:** ARSC
- **Descripción:** Resource Master Data - Log
- **Cantidad de campos:** 125
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ARSC.html

## Campos (125)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ResCode` | Internal Code | nVarChar | 50 | - |  |  |
| 2 | `VisResCode` | Resource No. | nVarChar | 50 | - |  |  |
| 3 | `Series` | Series | Int | 11 | [NNM1](NNM1.md) |  |  |
| 4 | `Number` | Number | Int | 11 | - |  |  |
| 5 | `CodeBars` | Bar Code | nVarChar | 254 | - |  |  |
| 6 | `ResName` | Resource Description | nVarChar | 200 | - |  |  |
| 7 | `FrgnName` | Description in Foreign Lang. | nVarChar | 200 | - |  |  |
| 8 | `ResType` | Resource Type | VarChar | 1 | - | M | `M` = Machine<br>`L` = Labor<br>`O` = Other |
| 9 | `ResGrpCod` | Resource Group | Int | 6 | [ORSB](ORSB.md) | 1 |  |
| 10 | `UnitOfMsr` | Unit of Measure | nVarChar | 100 | - |  |  |
| 11 | `PrchseRes` | Purchase Resource [Yes/No] | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 12 | `SellRes` | Sales Resource [Yes/No] | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 13 | `ProdRes` | Production Resource [Yes/No] | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 14 | `CardCode` | Preferred Vendor | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 15 | `NoDiscount` | No Discounts | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 16 | `IssueMthd` | Issue Method | VarChar | 1 | - | B | `B` = Backflush<br>`M` = Manual |
| 17 | `StdCost1` | Resource Cost 1 | Num | 19.6 | - |  |  |
| 18 | `StdCost2` | Resource Cost 2 | Num | 19.6 | - |  |  |
| 19 | `StdCost3` | Resource Cost 3 | Num | 19.6 | - |  |  |
| 20 | `StdCost4` | Resource Cost 4 | Num | 19.6 | - |  |  |
| 21 | `StdCost5` | Resource Cost 5 | Num | 19.6 | - |  |  |
| 22 | `StdCost6` | Resource Cost 6 | Num | 19.6 | - |  |  |
| 23 | `StdCost7` | Resource Cost 7 | Num | 19.6 | - |  |  |
| 24 | `StdCost8` | Resource Cost 8 | Num | 19.6 | - |  |  |
| 25 | `StdCost9` | Resource Cost 9 | Num | 19.6 | - |  |  |
| 26 | `StdCost10` | Resource Cost 10 | Num | 19.6 | - |  |  |
| 27 | `validFor` | Active | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 28 | `validFrom` | Active From | Date | 8 | - |  |  |
| 29 | `validTo` | Active To | Date | 8 | - |  |  |
| 30 | `frozenFor` | Inactive | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 31 | `frozenFrom` | Inactive From | Date | 8 | - |  |  |
| 32 | `frozenTo` | Inactive To | Date | 8 | - |  |  |
| 33 | `DfltWH` | Default Warehouse | nVarChar | 8 | - |  |  |
| 34 | `QueryGroup` | Properties | Int | 11 | - | 0 |  |
| 35 | `PicturName` | Picture | nVarChar | 200 | - |  |  |
| 36 | `UserText` | Item Remarks | Text | 16 | - |  |  |
| 37 | `QryGroup1` | Property 1 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 38 | `QryGroup2` | Property 2 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 39 | `QryGroup3` | Property 3 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 40 | `QryGroup4` | Property 4 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 41 | `QryGroup5` | Property 5 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 42 | `QryGroup6` | Property 6 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 43 | `QryGroup7` | Property 7 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 44 | `QryGroup8` | Property 8 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 45 | `QryGroup9` | Property 9 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 46 | `QryGroup10` | Property 10 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 47 | `QryGroup11` | Property 11 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 48 | `QryGroup12` | Property 12 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 49 | `QryGroup13` | Property 13 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 50 | `QryGroup14` | Property 14 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 51 | `QryGroup15` | Property 15 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 52 | `QryGroup16` | Property 16 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 53 | `QryGroup17` | Property 17 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 54 | `QryGroup18` | Property 18 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 55 | `QryGroup19` | Property 19 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 56 | `QryGroup20` | Property 20 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 57 | `QryGroup21` | Property 21 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 58 | `QryGroup22` | Property 22 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 59 | `QryGroup23` | Property 23 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 60 | `QryGroup24` | Property 24 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 61 | `QryGroup25` | Property 25 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 62 | `QryGroup26` | Property 26 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 63 | `QryGroup27` | Property 27 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 64 | `QryGroup28` | Property 28 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 65 | `QryGroup29` | Property 29 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 66 | `QryGroup30` | Property 30 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 67 | `QryGroup31` | Property 31 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 68 | `QryGroup32` | Property 32 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 69 | `QryGroup33` | Property 33 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 70 | `QryGroup34` | Property 34 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 71 | `QryGroup35` | Property 35 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 72 | `QryGroup36` | Property 36 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 73 | `QryGroup37` | Property 37 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 74 | `QryGroup38` | Property 38 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 75 | `QryGroup39` | Property 39 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 76 | `QryGroup40` | Property 40 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 77 | `QryGroup41` | Property 41 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 78 | `QryGroup42` | Property 42 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 79 | `QryGroup43` | Property 43 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 80 | `QryGroup44` | Property 44 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 81 | `QryGroup45` | Property 45 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 82 | `QryGroup46` | Property 46 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 83 | `QryGroup47` | Property 47 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 84 | `QryGroup48` | Property 48 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 85 | `QryGroup49` | Property 49 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 86 | `QryGroup50` | Property 50 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 87 | `QryGroup51` | Property 51 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 88 | `QryGroup52` | Property 52 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 89 | `QryGroup53` | Property 53 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 90 | `QryGroup54` | Property 54 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 91 | `QryGroup55` | Property 55 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 92 | `QryGroup56` | Property 56 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 93 | `QryGroup57` | Property 57 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 94 | `QryGroup58` | Property 58 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 95 | `QryGroup59` | Property 59 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 96 | `QryGroup60` | Property 60 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 97 | `QryGroup61` | Property 61 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 98 | `QryGroup62` | Property 62 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 99 | `QryGroup63` | Property 63 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 100 | `QryGroup64` | Property 64 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 101 | `CreateDate` | Date of Creation | Date | 8 | - |  |  |
| 102 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 103 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 104 | `ValidComm` | Active Remarks | nVarChar | 30 | - |  |  |
| 105 | `FrozenComm` | Inactive Remarks | nVarChar | 30 | - |  |  |
| 106 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 107 | `ObjType` | Object Type | nVarChar | 20 | - | 290 |  |
| 108 | `Deleted` | Deleted | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 109 | `UserSign2` | Updating User | Int | 6 | - |  |  |
| 110 | `Attachment` | Attachment | Text | 16 | - |  |  |
| 111 | `AtcEntry` | Attachment Entry | Int | 11 | - |  |  |
| 112 | `LastPurPrc` | Last Purchase Price | Num | 19.6 | - |  |  |
| 113 | `LastPurCur` | Last Purchase Currency | nVarChar | 3 | - |  |  |
| 114 | `LastPurDat` | Last Purchase Date | Date | 8 | - |  |  |
| 115 | `LstEvlPric` | Last Evaluated Price | Num | 19.6 | - |  |  |
| 116 | `LstEvlDate` | Date of Last Reval. Price | Date | 8 | - |  |  |
| 117 | `NumResUnit` | No. of Resource Units | Int | 11 | - | 1 |  |
| 118 | `TimeResUn` | Time per Resource Units | Int | 11 | - |  |  |
| 119 | `ResAlloc` | Resource Allocation | VarChar | 1 | - | S | `S` = On Start Date<br>`D` = On End Date<br>`F` = Start Date Forwards<br>`B` = End Date Backwards |
| 120 | `LinkItm` | Linked Item | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 121 | `RelCap1` | Relevant to single run capacity 1 | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 122 | `RelCap2` | Relevant to single run capacity 2 | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 123 | `RelCap3` | Relevant to single run capacity 3 | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 124 | `RelCap4` | Relevant to single run capacity 4 | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 125 | `UserSign` | User Signature | Int | 6 | - |  |  |

## Claves e índices (5)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ResCode, LogInstanc |
| ITEM_NAME | No | ResName |
| SALE | No | PrchseRes |
| PURCHASE | No | SellRes |
| PRODUCTION | No | ProdRes |
