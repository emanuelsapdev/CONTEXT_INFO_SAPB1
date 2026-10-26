# MSN4 - MRP Scenarios - Items Array

- **Tabla:** MSN4
- **Descripción:** MRP Scenarios - Items Array
- **Cantidad de campos:** 14
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MSN4.html

## Campos (14)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [OMSN](OMSN.md) |  |  |
| 2 | `ItemCode` | Item Code | nVarChar | 50 | - |  |  |
| 3 | `Selected` | Selected | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 4 | `TmpForMrp` | Is Temporary for MRP | VarChar | 1 | - | N |  |
| 5 | `WorDueDate` | Production Order Due Date | Date | 8 | - |  |  |
| 6 | `DsmDueDate` | Disassembly Order Due Date | Date | 8 | - |  |  |
| 7 | `NorDueDate` | Non Prd Order Doc. Due Date | Date | 8 | - |  |  |
| 8 | `Interval` | Order Intervals | Int | 6 | - |  |  |
| 9 | `Multiple` | Order Multiple | Num | 19.6 | - |  |  |
| 10 | `MinORdrQty` | Minimum Order Quantity | Num | 19.6 | - |  |  |
| 11 | `LeadTime` | Lead Time | Int | 11 | - |  |  |
| 12 | `prcrmntMtd` | Procurement Method | VarChar | 1 | - | B | `B` = Buy<br>`M` = Make |
| 13 | `ToleranDay` | Tolerance Day | Int | 11 | - |  |  |
| 14 | `CompoWH` | Component Warehouse | VarChar | 1 | - | B | `B` = From Bill of Materials Line<br>`P` = From Parent Item Document Line |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, ItemCode |
| ItemCode | No | ItemCode |
