# PQW2 - Purchase Quotation Generation Parameters

- **Tabla:** PQW2
- **Descripción:** Purchase Quotation Generation Parameters
- **Cantidad de campos:** 42
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/PQW2.html

## Campos (42)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `RunUser` | Run User ID | Int | 6 | - |  |  |
| 2 | `RunDate` | Job Running Date | Date | 8 | - |  |  |
| 3 | `RunTime` | Job Running Time | Int | 6 | - |  |  |
| 4 | `DocNum` | Document Number | Int | 11 | - |  |  |
| 5 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 6 | `VendorCode` | Vendor Code | nVarChar | 15 | - |  |  |
| 7 | `VendorName` | Vendor Name | nVarChar | 200 | - |  |  |
| 8 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 9 | `Dscription` | Item/Service Description | nVarChar | 200 | - |  |  |
| 10 | `WhsCode` | Warehouse Code | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 11 | `MinOrdrQty` | Minimum Order Quantity | Num | 19.6 | - |  |  |
| 12 | `InStock` | Item in Stock | Num | 19.6 | - |  |  |
| 13 | `Ordered` | Item Ordered | Num | 19.6 | - |  |  |
| 14 | `Committed` | Item Committed | Num | 19.6 | - |  |  |
| 15 | `ItmPerUnit` | Number of Items per Purchase Unit | Num | 19.6 | - |  |  |
| 16 | `BuyUnitMsr` | Purchasing UoM | nVarChar | 100 | - |  |  |
| 17 | `FreeTxt` | Free Text | nVarChar | 100 | - |  |  |
| 18 | `PQTGrpNum` | Purchase Quotation Group Number | Int | 11 | - |  |  |
| 19 | `PQTGrpSer` | Purchase Quotation Group Series | Int | 11 | - |  |  |
| 20 | `PQTGrpHW` | Purchase Quotation Group Manual | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 21 | `PQTReqQty` | Purchase Quotation: Required Qty | Num | 19.6 | - |  |  |
| 22 | `PQTSeries` | Purchase Quotation Series | Int | 11 | [NNM1](NNM1.md) |  |  |
| 23 | `PQTReqDate` | Purchase Quotation: Required Date | Date | 8 | - |  |  |
| 24 | `ValidUntil` | Valid Until Date | Date | 8 | - |  |  |
| 25 | `PRAbsEntry` | Purchase Request Number | Int | 11 | [OPRQ](OPRQ.md) |  |  |
| 26 | `PRDocNum` | Purchase Request Document Number | Int | 11 | - |  |  |
| 27 | `ReqName` | Requester Name | nVarChar | 155 | - |  |  |
| 28 | `PRLineNum` | Purchase Request Row Number | Int | 11 | - |  |  |
| 29 | `PRLineStat` | Purchase Request Row Status | VarChar | 1 | - |  |  |
| 30 | `DistRule` | Distribution Rule | nVarChar | 8 | - |  |  |
| 31 | `DistRule2` | Distribution Rule 2 | nVarChar | 8 | - |  |  |
| 32 | `DistRule3` | Distribution Rule 3 | nVarChar | 8 | - |  |  |
| 33 | `DistRule4` | Distribution Rule 4 | nVarChar | 8 | - |  |  |
| 34 | `DistRule5` | Distribution Rule 5 | nVarChar | 8 | - |  |  |
| 35 | `Project` | Project Code | nVarChar | 20 | - |  |  |
| 36 | `VendMfrNum` | Vendor Mfr Catalog No. | nVarChar | 17 | - |  |  |
| 37 | `ShipType` | Shipping Type | Int | 6 | - |  |  |
| 38 | `Buyer` | Buyer | Int | 11 | - |  |  |
| 39 | `PriceMode` | Price Mode | VarChar | 1 | - | N | `N` = Net<br>`G` = Gross |
| 40 | `UoMNum` | UoM Item Per Unit Numerator | Num | 19.6 | - |  |  |
| 41 | `UoMDen` | UoM Item Per Unit Denominator | Num | 19.6 | - |  |  |
| 42 | `IsNewPQ` | Is New Purchase Quotation | VarChar | 1 | - | Y | `N` = No<br>`Y` = Yes |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | RunUser, RunDate, RunTime, DocNum, LineNum |
