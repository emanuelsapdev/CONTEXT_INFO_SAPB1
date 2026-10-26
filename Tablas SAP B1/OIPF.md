# OIPF - Landed Costs

- **Tabla:** OIPF
- **Descripción:** Landed Costs
- **Cantidad de campos:** 66
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OIPF.html

## Campos (66)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `DocNum` | Document Number | Int | 11 | - |  |  |
| 3 | `DocDate` | Posting Date | Date | 8 | - |  |  |
| 4 | `DocDueDate` | Due Date | Date | 8 | - |  |  |
| 5 | `CardCode` | Vendor Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 6 | `SuppName` | Vendor Name | nVarChar | 200 | - |  |  |
| 7 | `AgentCode` | Subst. Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 8 | `AgentName` | Subst. Name | nVarChar | 200 | - |  |  |
| 9 | `DocStatus` | Document Status | VarChar | 1 | - | O | `C` = Closed<br>`O` = Open |
| 10 | `AgentNum` | File Number | nVarChar | 16 | - |  |  |
| 11 | `Descr` | Remarks | nVarChar | 250 | - |  |  |
| 12 | `Ref1` | Reference 1 | nVarChar | 11 | - |  |  |
| 13 | `Ref2` | Reference 2 | nVarChar | 11 | - |  |  |
| 14 | `DocCur` | Document Currency | nVarChar | 3 | - |  |  |
| 15 | `DocRate` | Document Rate | Num | 19.6 | - |  |  |
| 16 | `ExpCustom` | Projected Customs | Num | 19.6 | - |  |  |
| 17 | `ActCustom` | Act. Import Duty | Num | 19.6 | - |  |  |
| 18 | `Vat1` | Tax 2 | Num | 19.6 | - |  |  |
| 19 | `Vat2` | Tax 2 | Num | 19.6 | - |  |  |
| 20 | `BeforeVat` | Total Before Tax | Num | 19.6 | - |  |  |
| 21 | `DocTotal` | Document Total | Num | 19.6 | - |  |  |
| 22 | `CostSum` | Total Costs | Num | 19.6 | - |  |  |
| 23 | `DocTime` | Generation Time | Int | 6 | - |  |  |
| 24 | `Canceled` | Canceled | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 25 | `ExCustomFC` | Projected Customs (FC) | Num | 19.6 | - |  |  |
| 26 | `AcCustomFC` | Act. Import Duty in FC | Num | 19.6 | - |  |  |
| 27 | `Vat1FC` | Tax 1 (FC) | Num | 19.6 | - |  |  |
| 28 | `Vat2FC` | Tax 2 (FC) | Num | 19.6 | - |  |  |
| 29 | `BeforVatFC` | Total Before Tax (FC) | Num | 19.6 | - |  |  |
| 30 | `DocTotalFC` | Document Total (FC) | Num | 19.6 | - |  |  |
| 31 | `CostSumFC` | Total Costs (FC) | Num | 19.6 | - |  |  |
| 32 | `CloseDate` | Closing Date | Date | 8 | - |  |  |
| 33 | `Cost_Match` | Expenses Diff. for Reconciliation | Num | 19.6 | - |  |  |
| 34 | `C_Match_FC` | Expenses Diff. for Recon. (FC) | Num | 19.6 | - |  |  |
| 35 | `BillOfLad` | Bill of Lading No. | nVarChar | 20 | - |  |  |
| 36 | `TrnspCode` | Delivery Category | Int | 6 | [OSHP](OSHP.md) |  |  |
| 37 | `CostFactor` | Expenses Factor | Num | 19.6 | - |  |  |
| 38 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 39 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 40 | `Transfered` | Year Transfer | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 41 | `Instance` | Instance | Int | 6 | - | 0 |  |
| 42 | `TaxDate` | Document Date | Date | 8 | - |  |  |
| 43 | `Series` | Series | Int | 11 | - |  |  |
| 44 | `JdtNum` | Journal Number | Int | 11 | [OJDT](OJDT.md) |  |  |
| 45 | `JdtMemo` | Transaction Details | nVarChar | 254 | - |  |  |
| 46 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 47 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 48 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 69 |  |
| 49 | `ExCustomSC` | Projected Customs (SC) | Num | 19.6 | - |  |  |
| 50 | `ActCustSC` | Actual Customs (SC) | Num | 19.6 | - |  |  |
| 51 | `TtlCostSC` | Total Expenditure (SC) | Num | 19.6 | - |  |  |
| 52 | `VersionNum` | Version Number | nVarChar | 13 | - |  |  |
| 53 | `OpenForLaC` | Open For Landed Costs | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 54 | `incCustom` | Include Customs Expenses | VarChar | 1 | - | Y |  |
| 55 | `SeqCode` | Sequence Code | Int | 6 | - |  |  |
| 56 | `Serial` | Serial Number | Int | 11 | - |  |  |
| 57 | `SeriesStr` | Series String | nVarChar | 3 | - |  |  |
| 58 | `SubStr` | Subseries String | nVarChar | 3 | - |  |  |
| 59 | `BuildDesc` | Build Descriptor | nVarChar | 50 | - |  |  |
| 60 | `SupplCode` | Supplementary Code | nVarChar | 254 | - |  |  |
| 61 | `AtcEntry` | Attachment Entry | Int | 11 | - |  |  |
| 62 | `CustDate` | Customs Date | Date | 8 | - |  |  |
| 63 | `BPLId` | Branch | Int | 11 | [OBPL](OBPL.md) |  |  |
| 64 | `DPPStatus` | Data Protection Status | VarChar | 1 | - | N | `N` = None<br>`D` = Erased |
| 65 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 66 | `OwnerCode` | Document Owner | Int | 11 | [OHEM](OHEM.md) |  |  |

## Claves e índices (7)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry |
| NUM | Yes | DocNum, Instance, Series |
| SUPPLIER | No | CardCode |
| AGENT | No | AgentCode, AgentNum |
| CURRENCY | No | DocCur |
| SERIES | No | Series |
| OWNER_CODE | No | OwnerCode |
