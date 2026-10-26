# WVT4 - Variant -- embedded chart

- **Tabla:** WVT4
- **Descripción:** Variant -- embedded chart
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WVT4.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ParentId` | Parent Id | nVarChar | 40 | - |  |  |
| 2 | `Guid` | Guid | nVarChar | 40 | - |  |  |
| 3 | `ChartType` | Chart Type | nVarChar | 50 | - |  |  |
| 4 | `ShowLegend` | Show Legend | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 5 | `CtgrAxis1` | Category Axis 1 | nVarChar | 254 | - |  |  |
| 6 | `CtgrAxis2` | Category Axis 2 | nVarChar | 254 | - |  |  |
| 7 | `TimeAxis` | Time Axis | nVarChar | 254 | - |  |  |
| 8 | `Color` | Color | nVarChar | 254 | - |  |  |
| 9 | `Shape` | Shape | nVarChar | 254 | - |  |  |
| 10 | `BblWidth` | Bubble width | nVarChar | 254 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ParentId, Guid |
