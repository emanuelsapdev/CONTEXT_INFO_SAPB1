# PQW1 - Purchase Quotation Generation: Line Items

- **Tabla:** PQW1
- **Descripción:** Purchase Quotation Generation: Line Items
- **Cantidad de campos:** 26
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/PQW1.html

## Campos (26)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [OPQW](OPQW.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 4 | `Dscription` | Item/Service Description | nVarChar | 200 | - |  |  |
| 5 | `PQTReqDate` | Pur Quotation: Required Date | Date | 8 | - |  |  |
| 6 | `PQTReqQty` | Pur Quotation: Required Qty | Num | 19.6 | - |  |  |
| 7 | `BuyUnitMsr` | Purchasing UoM | nVarChar | 100 | - |  |  |
| 8 | `FreeTxt` | Free Text | nVarChar | 100 | - |  |  |
| 9 | `PQTGrpNum` | Pur. Quotation Group Number | Int | 11 | - |  |  |
| 10 | `PQTGrpSer` | Pur. Quotation Group Series | Int | 11 | - |  |  |
| 11 | `PQTGrpHW` | Pur. Quotation Group Manual | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 12 | `ValidUntil` | Valid Until Date | Date | 8 | - |  |  |
| 13 | `WhsCode` | Warehouse Code | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 14 | `PQTSeries` | Purchase Quotation Series | Int | 11 | [NNM1](NNM1.md) |  |  |
| 15 | `PRAbsEntry` | Purchase Request Number | Int | 11 | [OPRQ](OPRQ.md) |  |  |
| 16 | `ReqName` | Requester Name | nVarChar | 155 | - |  |  |
| 17 | `PRLineNum` | Purchase Request Row Number | Int | 11 | - |  |  |
| 18 | `PRLineStat` | Purchase Request Row Status | VarChar | 1 | - |  |  |
| 19 | `DistriRule` | Distribution Rule | nVarChar | 8 | - |  |  |
| 20 | `Project` | Project Code | nVarChar | 20 | - |  |  |
| 21 | `VendMfrNum` | Vendor Mfr Catalog No. | nVarChar | 17 | - |  |  |
| 22 | `ShipType` | Shipping Type | Int | 6 | - |  |  |
| 23 | `ItmPerUnit` | No. of Items per Purchase Unit | Num | 19.6 | - |  |  |
| 24 | `PriceMode` | Price Mode | VarChar | 1 | - | N | `N` = Net<br>`G` = Gross |
| 25 | `UoMNum` | UoM Item Per Unit Numerator | Num | 19.6 | - |  |  |
| 26 | `UoMDen` | UoM Item Per Unit Denominator | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineNum |
