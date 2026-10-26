# BEM2 - SAP Sustainability Footprint Management Transactional Data for Replication

- **Tabla:** BEM2
- **Descripción:** SAP Sustainability Footprint Management Transactional Data for Replication
- **Cantidad de campos:** 24
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/BEM2.html

## Campos (24)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `RowNumber` | Row Number of the PFMCOP Doc. Type | Int | 11 | - |  |  |
| 2 | `BEMDocType` | PFMCOP Doc. Type Code | Int | 11 | - |  |  |
| 3 | `BEMDocName` | PFMCOP Doc. Type Name | nVarChar | 60 | - |  |  |
| 4 | `ScopeKey` | Footprint Inventory Scope Identifier in PFMCOP | nVarChar | 36 | - |  |  |
| 5 | `RepId` | Replication Identifier | nVarChar | 36 | - |  |  |
| 6 | `StartDate` | Start Date | Date | 8 | - |  |  |
| 7 | `EndDate` | End Date | Date | 8 | - |  |  |
| 8 | `CreateDate` | Create Date | Date | 8 | - |  |  |
| 9 | `B1ObjCode` | B1 Object Code | nVarChar | 20 | - |  |  |
| 10 | `ItemCode` | Item Code | nVarChar | 60 | - |  |  |
| 11 | `WhseCode` | Warehouse Code | nVarChar | 60 | - |  |  |
| 12 | `UomCode` | Unit of Measure Code | nVarChar | 3 | - |  |  |
| 13 | `InQty` | In Quantity | Num | 19.6 | - |  |  |
| 14 | `OutQty` | Out Quantity | Num | 19.6 | - |  |  |
| 15 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 16 | `VendorCode` | Vendor Code | nVarChar | 60 | - |  |  |
| 17 | `WOREntry` | Production Order Internal Key | nVarChar | 60 | - |  |  |
| 18 | `RoleCode` | Material Role Code | nVarChar | 2 | - | MP | `MP` = Main Product<br>`BP` = By-Product |
| 19 | `RscCode` | Resource Code | nVarChar | 60 | - |  |  |
| 20 | `RscQty` | Resource Quantity | Num | 19.6 | - |  |  |
| 21 | `RscUomCode` | Resource Quantity UoM Code | nVarChar | 3 | - |  |  |
| 22 | `Project` | Project | nVarChar | 60 | - |  |  |
| 23 | `ToWhseCode` | To Warehouse Code | nVarChar | 60 | - |  |  |
| 24 | `CostCenter` | Cost Center | nVarChar | 8 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | RowNumber, BEMDocType, RepId |
| REP_ID | No | RepId |
