# MSN6 - MRP Job Details Header

- **Tabla:** MSN6
- **Descripción:** MRP Job Details Header
- **Cantidad de campos:** 30
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MSN6.html

## Campos (30)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `JobID` | Job ID | Int | 11 | - |  |  |
| 2 | `LineNum` | Line Number | Int | 11 | - |  |  |
| 3 | `ItemCode` | Item Code | nVarChar | 50 | - |  |  |
| 4 | `ItemDesc` | Item Description | nVarChar | 200 | - |  |  |
| 5 | `ItemGroup` | Item Group | nVarChar | 100 | - |  |  |
| 6 | `StockType` | Stock Type | VarChar | 1 | - |  |  |
| 7 | `ItemType` | Item Type | nVarChar | 100 | - |  |  |
| 8 | `PastDue` | Past Due Data | nVarChar | 50 | - |  |  |
| 9 | `PastDueRed` | Past Due is Red | VarChar | 1 | - |  |  |
| 10 | `PastDueGry` | Past Due is Grey | VarChar | 1 | - |  |  |
| 11 | `PastDueRmk` | Past Due Remarks | nVarChar | 200 | - |  |  |
| 12 | `HistData` | Historic Data | nVarChar | 50 | - |  |  |
| 13 | `HistRed` | Historic Data is Red | VarChar | 1 | - |  |  |
| 14 | `HistGrey` | Historic Data is Grey | VarChar | 1 | - |  |  |
| 15 | `ItmCodeRed` | Item Code is Red | VarChar | 1 | - |  |  |
| 16 | `ItmProcMtd` | Item Procurement Method | VarChar | 1 | - |  |  |
| 17 | `ItmLeadTm` | Item Lead Time | nVarChar | 20 | - |  |  |
| 18 | `ItmMinOrdQ` | Item Minimum Order Quantity | nVarChar | 20 | - |  |  |
| 19 | `ItmOrdMult` | Item Order Multiple | nVarChar | 20 | - |  |  |
| 20 | `ItmOrdIntv` | Item Order Interval | nVarChar | 20 | - |  |  |
| 21 | `ItmTolDays` | Item Tolerance Days | nVarChar | 20 | - |  |  |
| 22 | `ItmCmpWhs` | Item Component Warehouse | nVarChar | 8 | - |  |  |
| 23 | `MrpPrcMtd` | MRP Procurement Method | VarChar | 1 | - |  |  |
| 24 | `MrpLeadTm` | MRP Lead Time | nVarChar | 20 | - |  |  |
| 25 | `MrpMinOrdQ` | MRP Minimum Order Quantity | nVarChar | 20 | - |  |  |
| 26 | `MrpOrdMult` | MRP Order Multiple | nVarChar | 20 | - |  |  |
| 27 | `MrpOrdIntv` | MRP Order Interval | nVarChar | 20 | - |  |  |
| 28 | `MrpTolDays` | MRP Tolerance Days | nVarChar | 20 | - |  |  |
| 29 | `MrpCmpWhs` | MRP Component Warehouse | nVarChar | 8 | - |  |  |
| 30 | `PrvwEnbld` | Preview Enabled Flag | VarChar | 1 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | JobID, LineNum |
