# ORCJ - Resource Capacity Log

- **Tabla:** ORCJ
- **Descripción:** Resource Capacity Log
- **Cantidad de campos:** 24
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ORCJ.html

## Campos (24)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Id` | Primary Key | Int | 11 | - |  |  |
| 2 | `ResCode` | Internal Resource ID | nVarChar | 50 | [ORSC](ORSC.md) |  |  |
| 3 | `WhsCode` | Warehouse Code | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 4 | `CapDate` | Capacity Date | Date | 8 | - |  |  |
| 5 | `CapType` | Type of Capacity Entry | VarChar | 1 | - | I | `I` = Internal<br>`O` = Ordered<br>`C` = Committed<br>`U` = Consumed |
| 6 | `Capacity` | Capacity | Num | 19.6 | - |  |  |
| 7 | `SrcObjType` | Source Object Type | Int | 11 | - | -1 | `-1`<br>`202` = Production Order<br>`60` = Issue for Production<br>`59` = Receipt from Production<br>`17` = Sales Order<br>`15` = Delivery<br>`13` = A/R Invoice<br>`-13` = A/R Reserve Invoice<br>`14` = A/R Credit Memo<br>`165` = A/R Correction Invoice<br>`166` = A/R Correction Invoice Reversal<br>`16` = Returns<br>`22` = Purchase Order<br>`20` = Goods Receipt PO<br>`18` = A/P Invoice<br>`-18` = A/P Reserve Invoice<br>`19` = A/P Credit Memo<br>`163` = A/P Correction Invoice<br>`164` = A/P Correction Invoice Reversal<br>`21` = Goods Return |
| 8 | `SrcAbsEnt` | Source Absolute Entry | Int | 11 | - |  |  |
| 9 | `SrcLine` | Source Line Number | Int | 11 | - |  |  |
| 10 | `BaseObjTyp` | Base Object Type | Int | 11 | - | -1 | `-1`<br>`202` = Production Order |
| 11 | `BaseAbsEnt` | Base Absolute Entry | Int | 11 | - |  |  |
| 12 | `BaseLine` | Base Line Number | Int | 11 | - |  |  |
| 13 | `ActionType` | Action Type | Int | 6 | - | -1 | `-1`<br>`1` = Production Order - Create<br>`2` = Production Order - Close<br>`3` = Production Order - Reschedule<br>`4` = Production Order - Add Line<br>`5` = Production Order - Delete Line<br>`6` = Production Order - Update Line<br>`7` = Issue for Production - Create<br>`8` = Receipt from Production - Create<br>`9` = Sales Order - Create<br>`10` = Sales Order - Close<br>`11` = Sales Order - Cancel<br>`12` = Sales Order - Add Line<br>`13` = Sales Order - Delete Line<br>`14` = Sales Order - Update Line<br>`15` = Delivery - Create<br>`16` = Delivery - Close<br>`17` = Delivery - Cancel<br>`18` = A/R Invoice - Create<br>`19` = A/R Invoice - Cancel<br>`20` = A/R Credit Memo - Create<br>`21` = A/R Credit Memo - Cancel<br>`22` = Correction A/R Invoice - Create<br>`23` = Correction A/R Invoice Reversal - Create<br>`24` = Returns - Create<br>`25` = Returns - Cancel<br>`26` = Returns - Close<br>`27` = Purchase Order - Create<br>`28` = Purchase Order - Close<br>`29` = Purchase Order - Cancel<br>`30` = Purchase Order - Add Line<br>`31` = Purchase Order - Delete Line<br>`32` = Purchase Order - Update Line<br>`33` = Goods Receipt PO - Create<br>`34` = Goods Receipt PO - Close<br>`35` = Goods Receipt PO - Cancel<br>`36` = A/P Invoice - Create<br>`37` = A/P Invoice - Cancel<br>`38` = A/P Credit Memo - Create<br>`39` = A/P Credit Memo - Cancel<br>`40` = Correction A/P Invoice - Create<br>`41` = Correction A/P Invoice Reversal - Create<br>`42` = Goods Return - Create<br>`43` = Goods Return - Cancel<br>`44` = Goods Return - Close<br>`45` = A/R Invoice - Update<br>`46` = A/P Invoice - Update<br>`47` = A/R Reserve Invoice - Create<br>`48` = A/R Reserve Invoice - Update<br>`49` = A/R Reserve Invoice - Cancel<br>`50` = A/P Reserve Invoice - Create<br>`51` = A/P Reserve Invoice - Update<br>`52` = A/P Reserve Invoice - Cancel |
| 14 | `OwnObjTyp` | Owning Doc. Object Type | Int | 11 | - | -1 | `-1`<br>`202` = Production Order<br>`60` = Issue for Production<br>`59` = Receipt from Production<br>`17` = Sales Order<br>`15` = Delivery<br>`13` = A/R Invoice<br>`-13` = A/R Reserve Invoice<br>`14` = A/R Credit Memo<br>`165` = A/R Correction Invoice<br>`166` = A/R Correction Invoice Reversal<br>`16` = Returns<br>`22` = Purchase Order<br>`20` = Goods Receipt PO<br>`18` = A/P Invoice<br>`-18` = A/P Reserve Invoice<br>`19` = A/P Credit Memo<br>`163` = A/P Correction Invoice<br>`164` = A/P Correction Invoice Reversal<br>`21` = Goods Return |
| 15 | `OwnAbsEnt` | Owning Doc. Absolute Entry | Int | 11 | - |  |  |
| 16 | `OwnLine` | Owning Doc. Line Number | Int | 11 | - |  |  |
| 17 | `RevdObjTyp` | Reverted Object Type | Int | 11 | - | -1 | `-1`<br>`60` = Issue for Production |
| 18 | `RevdAbsEnt` | Reverted Absolute Entry | Int | 11 | - |  |  |
| 19 | `RevdLine` | Reverted Line Number | Int | 11 | - |  |  |
| 20 | `MemoSrc` | Memo Source | VarChar | 1 | - | - | `-`<br>`C` = Resource Capacity Form<br>`S` = Set Daily Internal Capacities Form |
| 21 | `Memo` | Memo | Text | 16 | - |  |  |
| 22 | `SngRunCap` | Single Run Capacity | Num | 19.6 | - |  |  |
| 23 | `MemoSrcSng` | Memo Source of Single Run Capacity | VarChar | 1 | - | - | `-`<br>`C` = Resource Capacity Form<br>`S` = Set Daily Internal Capacities Form |
| 24 | `MemoSng` | Memo of Single Run Capacity | Text | 16 | - |  |  |

## Claves e índices (4)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Id |
| RWDT | No | ResCode, WhsCode, CapDate, CapType |
| BASE_DOC | No | BaseObjTyp, BaseAbsEnt, BaseLine |
| OWNING_DOC | No | OwnObjTyp, OwnAbsEnt, OwnLine |
