# OWOR - Production Order

- **Tabla:** OWOR
- **Descripción:** Production Order
- **Cantidad de campos:** 63
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OWOR.html

## Campos (63)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `DocNum` | Document Number | Int | 11 | - |  |  |
| 3 | `Series` | Series | Int | 11 | [NNM1](NNM1.md) | 0 |  |
| 4 | `ItemCode` | Product No. | nVarChar | 50 | [OITT](OITT.md) |  |  |
| 5 | `Status` | Production Order Status | VarChar | 1 | - | P | `P` = Planned<br>`R` = Released<br>`L` = Closed<br>`C` = Canceled |
| 6 | `Type` | Production Order Type | VarChar | 1 | - | S | `S` = Standard<br>`P` = Special<br>`D` = Disassembly |
| 7 | `PlannedQty` | Planned Quantity - Header | Num | 19.6 | - |  |  |
| 8 | `CmpltQty` | Completed Quantity | Num | 19.6 | - |  |  |
| 9 | `RjctQty` | Rejected Quantity | Num | 19.6 | - |  |  |
| 10 | `PostDate` | Order Date | Date | 8 | - |  |  |
| 11 | `DueDate` | Due Date | Date | 8 | - |  |  |
| 12 | `OriginAbs` | Production Order Origin Entry | Int | 11 | - |  |  |
| 13 | `OriginNum` | Production Order Origin Number | Int | 11 | - |  |  |
| 14 | `OriginType` | Production Order Origin | VarChar | 1 | - | M | `M` = Manual<br>`R` = MRP<br>`S` = Sales Order<br>`U` = Upgrade<br>`P` = Production Order |
| 15 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 16 | `Comments` | Remarks | nVarChar | 254 | - |  |  |
| 17 | `CloseDate` | Closing Date | Date | 8 | - |  |  |
| 18 | `RlsDate` | Release Date | Date | 8 | - |  |  |
| 19 | `CardCode` | Customer Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 20 | `Warehouse` | Warehouse | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 21 | `Uom` | Inv. UoM in Production Order | nVarChar | 100 | - |  |  |
| 22 | `LineDirty` | Line Modified | Int | 11 | - |  |  |
| 23 | `JrnlMemo` | Journal Remarks | nVarChar | 254 | - |  |  |
| 24 | `TransId` | Transaction Number | Int | 11 | [OJDT](OJDT.md) |  |  |
| 25 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 26 | `Printed` | Printed | VarChar | 1 | - | N | `Y` = Copy<br>`N` = Original |
| 27 | `OcrCode` | Distribution Rule | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 28 | `PIndicator` | Period Indicator | nVarChar | 10 | [OPID](OPID.md) | ' ' |  |
| 29 | `OcrCode2` | Distribution Rule2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 30 | `OcrCode3` | Distribution Rule3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 31 | `OcrCode4` | Distribution Rule4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 32 | `OcrCode5` | Distribution Rule5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 33 | `SeqCode` | Sequence Code | Int | 6 | - |  |  |
| 34 | `Serial` | Serial Number | Int | 11 | - |  |  |
| 35 | `SeriesStr` | Series String | nVarChar | 3 | - |  |  |
| 36 | `SubStr` | Subseries String | nVarChar | 3 | - |  |  |
| 37 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 38 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 39 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 40 | `Project` | Project Code | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 41 | `SupplCode` | Supplementary Code | nVarChar | 254 | - |  |  |
| 42 | `UomEntry` | UoM Entry | Int | 11 | [OUOM](OUOM.md) | 0 |  |
| 43 | `PickRmrk` | Pick Remarks | nVarChar | 254 | - |  |  |
| 44 | `SysCloseDt` | System Closing Date | Date | 8 | - |  |  |
| 45 | `SysCloseTm` | System Closing Time | Int | 6 | - |  |  |
| 46 | `CloseVerNm` | Closing Version Number | nVarChar | 13 | - |  |  |
| 47 | `StartDate` | Start Date | Date | 8 | - |  |  |
| 48 | `ObjType` | Object Type | nVarChar | 20 | - | 202 |  |
| 49 | `ProdName` | Product Description | nVarChar | 200 | - |  |  |
| 50 | `Priority` | Priority | Int | 6 | - | 100 |  |
| 51 | `RouDatCalc` | Routing Date Calculation | VarChar | 1 | - | S | `S` = On Start Date<br>`D` = On End Date<br>`F` = Start Date Forwards<br>`B` = End Date Backwards |
| 52 | `UpdAlloc` | Update Allocation | VarChar | 1 | - | M | `M` = Manual<br>`C` = Calculated<br>`R` = Run Calculation |
| 53 | `CreateTS` | Create Time - Incl. Secs | Int | 11 | - |  |  |
| 54 | `UpdateTS` | Update Full Time | Int | 11 | - |  |  |
| 55 | `VersionNum` | Version Number | nVarChar | 13 | - |  |  |
| 56 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Upgrade<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Auto Summary<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 57 | `SAPPassprt` | Extended SAP Passport | Text | 16 | - |  |  |
| 58 | `AtcEntry` | Attachment Entry | Int | 11 | [OATC](OATC.md) |  |  |
| 59 | `Attachment` | Attachment | Text | 16 | - |  |  |
| 60 | `AsChild` | Parent set as component | VarChar | 1 | - | N | `Y` = Parent set as component<br>`N` = Parent not set as component |
| 61 | `LinkToObj` | Linked To | nVarChar | 20 | - | 17 | `202` = Production Order<br>`17` = Sales Order |
| 62 | `ProcItms` | Procure Items | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 63 | `ReopOriDoc` | Reopen Origin. Doc Cancel | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry |
| NUM | Yes | DocNum, PIndicator |
