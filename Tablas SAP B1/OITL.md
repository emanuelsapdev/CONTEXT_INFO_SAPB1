# OITL - Inventory Transactions Log

- **Tabla:** OITL
- **Descripción:** Inventory Transactions Log
- **Cantidad de campos:** 40
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OITL.html

## Campos (40)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `LogEntry` | Log Internal ID | Int | 11 | - |  |  |
| 2 | `TransId` | Transaction ID | Int | 11 | - |  |  |
| 3 | `ItemCode` | Item Code | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 4 | `ItemName` | Item Description | nVarChar | 200 | - |  |  |
| 5 | `ManagedBy` | Management Method | Int | 11 | - | 4 | `10000044` = BTN<br>`10000045` = SRN<br>`4` = ITM |
| 6 | `DocEntry` | Document Internal ID | Int | 11 | - |  |  |
| 7 | `DocLine` | Doc. Row Number | Int | 11 | - |  |  |
| 8 | `DocType` | Transact. Type | Int | 11 | - | -1 |  |
| 9 | `DocNum` | Doc. Number | Int | 11 | - |  |  |
| 10 | `BaseEntry` | Base Document Internal ID | Int | 11 | - | -1 |  |
| 11 | `BaseLine` | Base Document Row Number | Int | 11 | - | -1 |  |
| 12 | `BaseType` | Base Document Type | Int | 11 | - | -1 | `-1`<br>`0`<br>`13` = A/R Invoice<br>`15` = Delivery<br>`16` = Returns<br>`17` = Sales Order<br>`18` = A/P Invoice<br>`20` = Goods Receipt PO<br>`21` = Goods Return<br>`22` = Purchase Order<br>`23` = Sales Quotation<br>`59` = Goods Receipt<br>`67` = Inventory Transfer<br>`69` = Landed Costs<br>`163` = A/P Correction Invoice<br>`164` = A/P Correction Invoice Reversal<br>`165` = A/R Correction Invoice<br>`166` = A/R Correction Invoice Reversal<br>`202` = Production Order<br>`203` = A/R Down Payment<br>`204` = A/P Down Payment |
| 13 | `ApplyEntry` | Applied Document Internal ID | Int | 11 | - |  |  |
| 14 | `ApplyLine` | Applied Document Line Number | Int | 11 | - |  |  |
| 15 | `ApplyType` | Applied Document Type | Int | 11 | - | -1 |  |
| 16 | `DocDate` | Doc. Posting Date | Date | 8 | - |  |  |
| 17 | `CardCode` | BP Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 18 | `CardName` | BP Name | nVarChar | 200 | - |  |  |
| 19 | `DocQty` | Doc. Quantity | Num | 19.6 | - |  |  |
| 20 | `StockQty` | Stock Affecting Quantity | Num | 19.6 | - |  |  |
| 21 | `DefinedQty` | SnB Defined Quantity | Num | 19.6 | - |  |  |
| 22 | `StockEff` | Stock Effect | Int | 11 | - | 0 | `0` = ACCUM_EMPTY<br>`1` = ACCUM_ON_HAND<br>`2` = ACCUM_COMMITTED<br>`3` = ACCUM_ON_ORDER |
| 23 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 24 | `LocType` | Location Type | Int | 6 | - |  |  |
| 25 | `LocCode` | Location Code | nVarChar | 8 | - |  |  |
| 26 | `AppDocNum` | Applied Document Number | Int | 11 | - |  |  |
| 27 | `VersionNum` | Version Number | nVarChar | 13 | - |  |  |
| 28 | `Transfered` | Year Tranfer | VarChar | 1 | - | N |  |
| 29 | `Instance` | INSTANCE | Int | 6 | - | 0 |  |
| 30 | `SubLineNum` | Subrow Number | Int | 11 | - | -1 |  |
| 31 | `BSubLineNo` | Base Subrow Number | Int | 11 | - | -1 |  |
| 32 | `AppSubLine` | Applied Subrow Number | Int | 11 | - | -1 |  |
| 33 | `ActBaseTp` | Actual Base Type | Int | 11 | - | -1 |  |
| 34 | `ActBaseEnt` | Actual Base Entry | Int | 11 | - |  |  |
| 35 | `ActBaseLn` | Actual Base Line | Int | 11 | - | -1 |  |
| 36 | `ActBasSubL` | Actual Base Subline | Int | 11 | - | -1 |  |
| 37 | `AllocateTp` | Allocate Document Type | Int | 11 | - | -1 |  |
| 38 | `AllocatEnt` | Allocate Document Entry | Int | 11 | - | -1 |  |
| 39 | `AllocateLn` | Allocate Document Line | Int | 11 | - | -1 |  |
| 40 | `CreateTime` | Creation Time | Int | 6 | - | 0 |  |

## Claves e índices (9)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | LogEntry |
| DOC_INFO | No | ManagedBy, DocType, DocEntry, DocLine, SubLineNum |
| BASEREF | No | BaseType, BaseEntry, BaseLine, BSubLineNo |
| APPLYREF | No | ApplyType, ApplyEntry, ApplyLine, AppSubLine |
| TRANSID | No | TransId |
| ACTUAL_INF | No | ManagedBy, ActBaseTp, ActBaseEnt, ActBaseLn, ActBasSubL |
| ALLOC_REF | No | AllocateTp, AllocatEnt, AllocateLn |
| DOC_REF | No | DocType, DocEntry, DocLine, LogEntry |
| ITEM_CODE | No | ItemCode, LocCode, ManagedBy, Instance, ApplyEntry, ApplyType, LogEntry |
