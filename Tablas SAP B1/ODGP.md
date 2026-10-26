# ODGP - Document Generation Parameter Sets

- **Tabla:** ODGP
- **Descripción:** Document Generation Parameter Sets
- **Cantidad de campos:** 61
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ODGP.html

## Campos (61)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `SetName` | Set Name | nVarChar | 20 | - |  |  |
| 3 | `SetDesc` | Set Description | nVarChar | 100 | - |  |  |
| 4 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 5 | `ModifyDate` | Last Modified | Date | 8 | - |  |  |
| 6 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 7 | `Target` | Target Document Type | nVarChar | 20 | - | -1 | `-1`<br>`17` = Sales Order<br>`15` = Delivery<br>`16` = Returns<br>`13` = A/R Invoice |
| 8 | `PostDate` | Posting Date | Date | 8 | - |  |  |
| 9 | `TaxDate` | Document Date | Date | 8 | - |  |  |
| 10 | `Series` | Series | Int | 11 | - |  |  |
| 11 | `Items` | Items Documents Summary | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 12 | `ItemSmmry` | Items Summary Method | VarChar | 1 | - | N | `N` = No Summary<br>`I` = Summary by Items<br>`D` = Summary by Documents |
| 13 | `Service` | Service Documents Summary | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 14 | `ServSmmry` | Service Summary Method | VarChar | 1 | - | N | `N` = No Summary<br>`D` = Summary by Documents |
| 15 | `ExchgRate` | Exchange Rate | VarChar | 1 | - | C | `D` = Use Base Doc. and Row Rate<br>`B` = Use Base Row Rate<br>`C` = Use Current Rate |
| 16 | `CreatDraft` | Create Drafts | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 17 | `BaseQUT` | Sales Quotation Summary | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 18 | `BaseRDR` | Order Summary | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 19 | `BaseDLN` | Delivery Summary | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 20 | `BaseRDN` | Returns Summary | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 21 | `BaseResINV` | A/R Reserve Invoice Summary | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 22 | `ExpndSel` | Expanded Selection Criteria | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 23 | `SortField` | Sort Field | nVarChar | 100 | - | DocNum | `DocNum` = Document Number<br>`DocDate` = Posting Date<br>`DocDueDate` = Due Date<br>`NumAtCard` = BP Reference No.<br>`DocTotal` = Document Amount<br>`SlpCode` = Sales Employee |
| 24 | `Consolidat` | Consolidate | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 25 | `ExpandCons` | Expanded Consolidation Options | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 26 | `RCNSummary` | Reference Document | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 27 | `ChainCode` | Retail Chain | Int | 11 | - |  |  |
| 28 | `OredrNum1` | Order No. From | Int | 11 | - |  |  |
| 29 | `OredrNum2` | To | Int | 11 | - |  |  |
| 30 | `Direct` | Direct | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 31 | `Indirect` | Indirect | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 32 | `DoReport` | Overview of Invoice Deliveries | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 33 | `FileExport` | File Export | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 34 | `SavePath` | File Path | Text | 16 | - |  |  |
| 35 | `DealNum` | Closing No. | nVarChar | 12 | - |  |  |
| 36 | `UseDirect` | Direct/Indirect | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 37 | `NoItmCode` | Drop Item No. Where Cat. No. E | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 38 | `OnData` | Missing Data | VarChar | 1 | - | N | `N` = Skip to Next Document<br>`B` = Skip to Next Customer<br>`W` = Ask for User Confirmation |
| 39 | `OnLedger` | Bookkeeping Alert | VarChar | 1 | - | N | `N` = Skip to Next Document<br>`B` = Skip to Next Customer<br>`W` = Ask for User Confirmation |
| 40 | `OnInvnt` | Warehouse Alert | VarChar | 1 | - | N | `N` = Skip to Next Document<br>`B` = Skip to Next Customer<br>`W` = Ask for User Confirmation |
| 41 | `Summary` | Summary | nVarChar | 250 | - |  |  |
| 42 | `AltItmDocs` | Process docsc with alt. items | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 43 | `PartDelivr` | Partial Delivery | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 44 | `ConsiderBP` | Consider BP | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 45 | `ConsiderTy` | Consider Type | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 46 | `EDocGenTyp` | Electr. Doc. Generation Type | VarChar | 1 | - | D | `N` = Not Relevant<br>`G` = Generate<br>`L` = Generate - Later<br>`S` = Send<br>`R` = Send - Later<br>`D` = Use Defaults |
| 47 | `ESeries` | Electronic Series | Int | 6 | [NNM4](NNM4.md) |  |  |
| 48 | `EDocNum` | Electronic Document Number | nVarChar | 20 | - |  |  |
| 49 | `ReopOriRdr` | Reopen Origin. Order by Return | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 50 | `ReopManCls` | Reop. Man. Closed/Canc. Orders | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 51 | `SeqCode` | Target Doc. NF Sequence Code | Int | 6 | - |  |  |
| 52 | `UseBaseSeq` | Use Base Document NF Sequence | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 53 | `OnSeqCode` | Missing NF Sequence | VarChar | 1 | - | N | `N` = Skip to Next Document<br>`T` = Use NF Sequence from Step 2 |
| 54 | `BPLId` | Branch | Int | 11 | [OBPL](OBPL.md) |  |  |
| 55 | `BlckFrOnly` | Block Docs. with Zero Items | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 56 | `DocSubType` | Document Sub-Type | nVarChar | 2 | - | -- | `--` = Bill of Supply<br>`GA` = GST Tax Invoice |
| 57 | `EDocDflt` | Apply El. Doc. Defaults | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 58 | `EDocMapID` | Electronic Document Format Mapping | Int | 11 | - |  |  |
| 59 | `VatDate` | VAT Allocation Date | Date | 8 | - |  |  |
| 60 | `BsPrcMode` | Base Document Price Mode | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 61 | `Status` | Wizard Status | VarChar | 1 | - | P | `F` = Finished<br>`P` = Pending |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| SET_NAME | Yes | SetName |
