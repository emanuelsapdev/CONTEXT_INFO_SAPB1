# ORCM - Recommendation Data

- **Tabla:** ORCM
- **Descripción:** Recommendation Data
- **Cantidad de campos:** 33
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ORCM.html

## Campos (33)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `ObjAbs` | Document Internal Number | Int | 11 | - |  |  |
| 3 | `ObjType` | Document Number | Int | 11 | - |  |  |
| 4 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 5 | `DueDate` | Order Due Date | Date | 8 | - |  |  |
| 6 | `OrderType` | Order Type | VarChar | 1 | - | P | `P` = Purchase Order<br>`W` = Production Order<br>`T` = Inventory Transfer Request<br>`Q` = Purchase Quotation<br>`R` = Purchase Request |
| 7 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 8 | `UOM` | Buy or Inventory UoM | nVarChar | 100 | - |  |  |
| 9 | `CardCode` | Preferred Vendor | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 10 | `Warehouse` | Warehouse | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 11 | `Price` | Price After Discount | Num | 19.6 | - |  |  |
| 12 | `Currency` | Price Currency | nVarChar | 3 | - |  |  |
| 13 | `Origin` | Order Origin | VarChar | 1 | - | M | `M` = MRP |
| 14 | `Status` | Order Status | VarChar | 1 | - | O | `O` = Opened<br>`A` = Accepted<br>`P` = Processed<br>`D` = Deleted |
| 15 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 16 | `DocDate` | Generation Date | Date | 8 | - |  |  |
| 17 | `DocTime` | Generation Time | Int | 6 | - |  |  |
| 18 | `BPLid` | Business Place ID | Int | 11 | - | -1 |  |
| 19 | `PriceBefDi` | Unit Price | Num | 19.6 | - |  |  |
| 20 | `DiscPrcnt` | Discount % Per Row | Num | 19.6 | - |  |  |
| 21 | `ReleasDate` | Release Date | Date | 8 | - |  |  |
| 22 | `PriceAftV` | Price after VAT | Num | 19.6 | - |  |  |
| 23 | `FromWhse` | From Warehouse | nVarChar | 8 | - |  |  |
| 24 | `FstReqDate` | First Request Date | Date | 8 | - |  |  |
| 25 | `UomEntry` | UoM Entry | Int | 11 | - |  |  |
| 26 | `NumPerMsr` | UoM Value | Num | 19.6 | - |  |  |
| 27 | `AgrNo` | Agreement No. | Int | 11 | [OOAT](OOAT.md) |  |  |
| 28 | `AgrLnNum` | Agreement Row Number | Int | 11 | - |  |  |
| 29 | `UseDiscnt` | Use BP Special Price | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 30 | `PriceMode` | Price Mode | VarChar | 1 | - |  | `N` = Net<br>`G` = Gross |
| 31 | `RouDatCalc` | Routing Date Calculation | VarChar | 1 | - |  | `S` = On Start Date<br>`D` = On End Date<br>`F` = Start Date Onwards<br>`B` = End Date Backwards |
| 32 | `UoMNum` | UoM Item Per Unit Numerator | Num | 19.6 | - |  |  |
| 33 | `UoMDen` | UoM Item Per Unit Denominator | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry |
