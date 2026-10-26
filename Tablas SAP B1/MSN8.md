# MSN8 - MRP Job Recommendations

- **Tabla:** MSN8
- **Descripción:** MRP Job Recommendations
- **Cantidad de campos:** 27
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MSN8.html

## Campos (27)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `JobID` | Job ID | Int | 11 | - |  |  |
| 2 | `LineNum` | Line Number | Int | 11 | - |  |  |
| 3 | `OrderType` | Order Type | VarChar | 1 | - |  |  |
| 4 | `ItemCode` | Item Code | nVarChar | 50 | - |  |  |
| 5 | `ItemDesc` | Item Description | nVarChar | 200 | - |  |  |
| 6 | `ItemGroup` | Item Group | nVarChar | 100 | - |  |  |
| 7 | `Manufactr` | Manufacturer | nVarChar | 100 | - |  |  |
| 8 | `BarCode` | Bar Code | nVarChar | 100 | - |  |  |
| 9 | `Quantity` | Quantity | nVarChar | 50 | - |  |  |
| 10 | `TotQtyInv` | Total Qty in Inventory UoM | nVarChar | 50 | - |  |  |
| 11 | `UOM` | UoM Code | nVarChar | 50 | - |  |  |
| 12 | `UoMName` | UoM Name | nVarChar | 100 | - |  |  |
| 13 | `NumPerMsr` | Number per Unit of Measure | nVarChar | 50 | - |  |  |
| 14 | `ReleasDate` | Release Date | Date | 8 | - |  |  |
| 15 | `DueDate` | Due Date | Date | 8 | - |  |  |
| 16 | `VendorCode` | Vendor Code | nVarChar | 15 | - |  |  |
| 17 | `VendorName` | Vendor Name | nVarChar | 200 | - |  |  |
| 18 | `Price` | Price | nVarChar | 50 | - |  |  |
| 19 | `DiscPrcnt` | Discount % | nVarChar | 50 | - |  |  |
| 20 | `PriceAftV` | Price After VAT | nVarChar | 50 | - |  |  |
| 21 | `Total` | Total | nVarChar | 50 | - |  |  |
| 22 | `FromWhse` | From Warehouse | nVarChar | 8 | - |  |  |
| 23 | `ToWhse` | To Warehouse | nVarChar | 8 | - |  |  |
| 24 | `Exception` | Exception | nVarChar | 100 | - |  |  |
| 25 | `FstReqDate` | First Request Date | Date | 8 | - |  |  |
| 26 | `PriceMode` | Price Mode | nVarChar | 20 | - |  |  |
| 27 | `PrvwEnbld` | Preview Enabled Flag | VarChar | 1 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | JobID, LineNum |
