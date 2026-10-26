# OMSN - MRP Scenarios

- **Tabla:** OMSN
- **Descripción:** MRP Scenarios
- **Cantidad de campos:** 58
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OMSN.html

## Campos (58)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `MsnCode` | MRP Scenario Code | nVarChar | 30 | - |  |  |
| 3 | `Descr` | Description | nVarChar | 100 | - |  |  |
| 4 | `GrpPeriods` | Group Data into Periods of | VarChar | 1 | - | D | `D` = Days<br>`W` = Weeks<br>`M` = Months |
| 5 | `PeriodsLen` | Group Data into Periods of | Int | 11 | - | 1 |  |
| 6 | `StartDate` | Report Start Date | Date | 8 | - |  |  |
| 7 | `EndDate` | Report End Date | Date | 8 | - |  |  |
| 8 | `MaxLdTime` | Maximum Cumulative Lead Time | Int | 11 | - |  |  |
| 9 | `HldaysProd` | Holidays for Production | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 10 | `HldaysPurc` | Holidays for Purchase | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 11 | `ItmFrom` | Items Codes From | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 12 | `ItmTo` | Items Codes To | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 13 | `ItmGrp` | Items Groups | Int | 11 | [OITB](OITB.md) |  |  |
| 14 | `ItmQryGrp` | Item Summary Report Group | nVarChar | 250 | - |  |  |
| 15 | `ExistStock` | Consider Existing Inventory | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 16 | `PurchOrder` | Consider Purchase Orders | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 17 | `SalesOrder` | Consider Sales Orders | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 18 | `WorkOrder` | Consider Work Orders | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 19 | `MinStckLvl` | Minimum Inventory Level | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 20 | `FCTAbs` | Forecast Absolute Entry | Int | 11 | [OFCT](OFCT.md) |  |  |
| 21 | `SortBy` | Sort By | VarChar | 1 | - | L | `L` = Assembly Sequence<br>`C` = Item Number<br>`N` = Item Description<br>`G` = Item Group |
| 22 | `ItmReq` | Items Without Requirement | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 23 | `Simulation` | Is Scenario a Simulation | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 24 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 25 | `UpdateBy` | Update By | nVarChar | 20 | - |  |  |
| 26 | `LastExecDa` | Last Execute Date | Date | 8 | - |  |  |
| 27 | `AllItems` | All Items | VarChar | 1 | - | Y |  |
| 28 | `ByCompany` | By Company | VarChar | 1 | - | Y |  |
| 29 | `IncHisData` | Include Historical Data | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 30 | `ResInv` | Reserve Invoice | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 31 | `Wtrq` | Inventory Transfer Request | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 32 | `InvtLevel` | Inventory Level | VarChar | 1 | - | D | `D`<br>`R` = Required<br>`I` = Minimum<br>`A` = Maximum<br>`M` = Minimum - Maximum |
| 33 | `RcmPO` | Recommend Purchase Order | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 34 | `RcmWO` | Recommend Production Order | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 35 | `RcmWTRQ` | Recommend ITRQ | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 36 | `RCMDefWhs` | Recommend to Default Warehouse | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 37 | `OnlyNettbl` | Only Nettable | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 38 | `ExpandedPO` | Expanded Purchase Order | VarChar | 1 | - | N |  |
| 39 | `ExpandedSO` | Expanded Sales Order | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 40 | `RcmCalDate` | Recommendation Calculated Date | Date | 8 | - |  |  |
| 41 | `RcmCalTime` | Recommendation Calculated Time | Int | 11 | - |  |  |
| 42 | `PurchOAT` | Blanket Purchase Agreement | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 43 | `SalesOAT` | Blanket Sales Agreement | VarChar | 1 | - | Y |  |
| 44 | `Rots` | Recurring Order Transactions | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 45 | `ExpdResINV` | Expanded Reserve Invoice | VarChar | 1 | - | N |  |
| 46 | `ExpdWOR` | Expanded Production Order | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 47 | `IgnoreCLT` | Ignore Cumulative Lead Time | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 48 | `PurchReq` | Consider Purchase Request | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 49 | `PurchQuota` | Consider Purchase Quotations | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 50 | `SalesQuota` | Consider Sales Quotations | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 51 | `ExpdPurReq` | Expanded Purchase Request | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 52 | `ExpdPQuota` | Expanded Purchase Quotations | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 53 | `ExpdSQuota` | Expanded Sales Quotations | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 54 | `ExpdPAgree` | Expanded Purchase Agreements | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 55 | `ExpdSAgree` | Expanded Sales Agreements | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 56 | `ExpdTraReq` | Expanded Transfer Request | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 57 | `DisSelItem` | Display Selected Item Only | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 58 | `PlanHorizn` | Plan Horizon | Text | 16 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| MSN_CODE | Yes | MsnCode |
