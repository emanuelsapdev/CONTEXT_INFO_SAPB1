# OKPI - Key Performance Indicator Package

- **Tabla:** OKPI
- **Descripción:** Key Performance Indicator Package
- **Cantidad de campos:** 25
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OKPI.html

## Campos (25)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `Code` | KPI Code | nVarChar | 250 | - |  |  |
| 3 | `Name` | KPI Name | nVarChar | 250 | - |  |  |
| 4 | `Desc` | Description | nVarChar | 254 | - |  |  |
| 5 | `ValueType` | Value Type | nVarChar | 200 | - |  |  |
| 6 | `ValueQid` | Value Query Number | Int | 11 | - |  |  |
| 7 | `ViewName` | Value View Name | nVarChar | 250 | - |  |  |
| 8 | `ViewCtg` | View Catalog | nVarChar | 250 | - |  |  |
| 9 | `ViewSyn` | View Synonym | nVarChar | 250 | - |  |  |
| 10 | `TrendType` | Trend Type | nVarChar | 250 | - |  |  |
| 11 | `TrendQid` | Trend Query Number | Int | 11 | - |  |  |
| 12 | `GoalValue` | Goal Value | Num | 19.6 | - |  |  |
| 13 | `GoalQid` | Goal Query Number | nVarChar | 11 | - |  |  |
| 14 | `GoalDesc` | Goal Description | nVarChar | 250 | - |  |  |
| 15 | `CalcFrml` | Calculation Formula | nVarChar | 250 | - |  |  |
| 16 | `Visible` | Visible For Front End | VarChar | 1 | - | Y |  |
| 17 | `SBetter` | Smaller Value is Better | VarChar | 1 | - | Y |  |
| 18 | `Author` | Creator | nVarChar | 32 | - |  |  |
| 19 | `Version` | Version | nVarChar | 13 | - |  |  |
| 20 | `CreateDate` | Create Date | Date | 8 | - |  |  |
| 21 | `CreateTime` | Create Time | Int | 6 | - |  |  |
| 22 | `IsSystem` | Is System | VarChar | 1 | - | N |  |
| 23 | `MeasUnit` | Measuring Unit | nVarChar | 50 | - | 0 |  |
| 24 | `RevSign` | Reverse Sign | VarChar | 1 | - | N |  |
| 25 | `Unit` | Unit | nVarChar | 250 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| NAME | Yes | Name |
