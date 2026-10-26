# ORCP - Recurring Transaction Template

- **Tabla:** ORCP
- **Descripción:** Recurring Transaction Template
- **Cantidad de campos:** 20
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ORCP.html

## Campos (20)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `Code` | Template Code | nVarChar | 8 | - |  |  |
| 3 | `Dscription` | Description | nVarChar | 50 | - |  |  |
| 4 | `IsRemoved` | Is Removed | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 5 | `DocObjType` | Linked Document Type | nVarChar | 20 | - | -1 | `-1`<br>`23` = Sales Quotation<br>`17` = Sales Order<br>`15` = Delivery<br>`234000031` = Returns Request<br>`16` = Return<br>`-203` = A/R Down Payment Request<br>`203` = A/R Down Payment Invoice<br>`13` = A/R Invoice<br>`14` = A/R Credit Memo<br>`-13` = A/R Reserve Invoice<br>`1470000113` = Purchase Request<br>`540000006` = Purchase Quotation<br>`22` = Purchase Order<br>`20` = Goods Receipt PO<br>`234000032` = Goods Returns Request<br>`21` = Goods Return<br>`-204` = A/P Down Payment Request<br>`204` = A/P Down Payment Invoice<br>`18` = A/P Invoice<br>`19` = A/P Credit Memo<br>`-18` = A/P Reserve Invoice<br>`59` = Goods Receipt<br>`60` = Goods Issue<br>`1250000001` = Inventory Transfer Request<br>`67` = Inventory Transfer |
| 6 | `DraftEntry` | Linked Draft Entry | Int | 11 | [ODRF](ODRF.md) |  |  |
| 7 | `Frequency` | Frequency | VarChar | 1 | - | M | `D` = Daily<br>`W` = Weekly<br>`X` = Every 2 Weeks<br>`M` = Monthly<br>`P` = Every 2 Months<br>`Q` = Quarterly<br>`S` = Semiannually<br>`A` = Annually<br>`O` = One Time |
| 8 | `Remind` | Sub-Frequency | Int | 6 | - | 1001 | `-1`<br>`1` = On Sunday<br>`2` = On Monday<br>`3` = On Tuesday<br>`4` = On Wednesday<br>`5` = On Thursday<br>`6` = On Friday<br>`7` = On Saturday<br>`101` = Every 1<br>`102` = Every 2<br>`103` = Every 3<br>`104` = Every 4<br>`105` = Every 5<br>`106` = Every 6<br>`107` = Every 7<br>`108` = Every 8<br>`109` = Every 9<br>`110` = Every 10<br>`111` = Every 11<br>`112` = Every 12<br>`113` = Every 13<br>`114` = Every 14<br>`115` = Every 15<br>`116` = Every 16<br>`117` = Every 17<br>`118` = Every 18<br>`119` = Every 19<br>`120` = Every 20<br>`121` = Every 21<br>`122` = Every 22<br>`123` = Every 23<br>`124` = Every 24<br>`125` = Every 25<br>`126` = Every 26<br>`127` = Every 27<br>`128` = Every 28<br>`129` = Every 29<br>`130` = Every 30<br>`131` = Every 31<br>`145` = Every 45<br>`160` = Every 60<br>`1001` = On 1<br>`1002` = On 2<br>`1003` = On 3<br>`1004` = On 4<br>`1005` = On 5<br>`1006` = On 6<br>`1007` = On 7<br>`1008` = On 8<br>`1009` = On 9<br>`1010` = On 10<br>`1011` = On 11<br>`1012` = On 12<br>`1013` = On 13<br>`1014` = On 14<br>`1015` = On 15<br>`1016` = On 16<br>`1017` = On 17<br>`1018` = On 18<br>`1019` = On 19<br>`1020` = On 20<br>`1021` = On 21<br>`1022` = On 22<br>`1023` = On 23<br>`1024` = On 24<br>`1025` = On 25<br>`1026` = On 26<br>`1027` = On 27<br>`1028` = On 28<br>`1029` = On 29<br>`1030` = On 30<br>`1031` = On 31 |
| 9 | `StartDate` | Execution Start Date | Date | 8 | - |  |  |
| 10 | `EndDate` | Execution End Date | Date | 8 | - |  |  |
| 11 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 12 | `CreateUser` | Created by User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 13 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 14 | `CreateTime` | Creation Time | Int | 6 | - |  |  |
| 15 | `UpdateUser` | Updated by User | nVarChar | 6 | [OUSR](OUSR.md) |  |  |
| 16 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 17 | `UpdateTime` | Update Time | Int | 6 | - |  |  |
| 18 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Upgrade<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Auto Summary<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 19 | `PriceUpdat` | Prices Update | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 20 | `CardCode` | Customer/Vendor Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
