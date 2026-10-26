# PMG9 - Project Management - Charged Document Lines Log - Used by Billing Wizard

- **Tabla:** PMG9
- **Descripción:** Project Management - Charged Document Lines Log - Used by Billing Wizard
- **Cantidad de campos:** 19
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/PMG9.html

## Campos (19)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | - |  |  |
| 2 | `LineID` | Row No. | Int | 11 | - |  |  |
| 3 | `BWRefID` | Billing Wizard Reference ID | Int | 11 | - |  |  |
| 4 | `TargetType` | Target Document Type | Int | 11 | - | -1 | `-1`<br>`15` = Delivery<br>`13` = A/R Invoice |
| 5 | `TargetAbs` | Target Document Abs. Entry | Int | 11 | - |  |  |
| 6 | `TargetNum` | Target Document Number | Int | 11 | - |  |  |
| 7 | `TargetLine` | Target Document Line Number | Int | 11 | - |  |  |
| 8 | `SubProjID` | Subproject ID | Int | 11 | - | -1 |  |
| 9 | `StageID` | Stage ID | Int | 11 | - |  |  |
| 10 | `SourceType` | Source Document Type | Int | 11 | - | -1 | `-1`<br>`18` = A/P Invoice<br>`23` = Sales Quotation<br>`17` = Sales Order<br>`13002` = A/R Reserve Invoice<br>`15` = Delivery<br>`33` = Activity<br>`202` = Work Order<br>`234000024` = Timesheet |
| 11 | `SourceAbs` | Source Document Abs. Entry | Int | 11 | - |  |  |
| 12 | `SourceNum` | Source Document Number | Int | 11 | - |  |  |
| 13 | `SourceLine` | Source Document Line Number | Int | 11 | - |  |  |
| 14 | `Charged` | Charged | Num | 19.6 | - |  |  |
| 15 | `ChargedQty` | Charged Quantity | Num | 19.6 | - |  |  |
| 16 | `DestType` | Destination Table Type | Int | 11 | - | -1 | `-1`<br>`234000021` = Project Management Document<br>`234000022` = Project Management Subproject<br>`234000024` = Time Sheet Document |
| 17 | `DestArr` | Destination Table Array | Int | 11 | - | -1 | `-1`<br>`1` = Time Sheet Lines<br>`4` = Stage Documents<br>`6` = Stage Activities<br>`7` = Stage Workorders |
| 18 | `DestAbs` | Destination Table Abs. Entry | Int | 11 | - |  |  |
| 19 | `DestLine` | Destination Table Line Number | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, BWRefID, TargetType, TargetAbs, LineID |
