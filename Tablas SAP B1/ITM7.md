# ITM7 - Asset Item Depreciation Params

- **Tabla:** ITM7
- **Descripción:** Asset Item Depreciation Params
- **Cantidad de campos:** 17
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ITM7.html

## Campos (17)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 2 | `PeriodCat` | Period Category | nVarChar | 10 | - |  |  |
| 3 | `DprArea` | Depreciation Area | nVarChar | 15 | [ODPA](ODPA.md) |  |  |
| 4 | `VisOrder` | Visual Order | Int | 11 | - |  |  |
| 5 | `DprStart` | Depreciation Start Date | Date | 8 | - |  |  |
| 6 | `DprEnd` | Depreciation End Date | Date | 8 | - |  |  |
| 7 | `UsefulLife` | Useful Life | Int | 11 | - |  |  |
| 8 | `RemainLife` | Remaining Life | Num | 19.6 | - |  |  |
| 9 | `DprType` | Depreciation Type | nVarChar | 15 | [ODTP](ODTP.md) |  |  |
| 10 | `DprTypeC` | Depr. Type Calculation | nVarChar | 15 | [ODTP](ODTP.md) |  |  |
| 11 | `UsefulLfeC` | Useful Life Calculation | Int | 11 | - |  |  |
| 12 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 13 | `ObjType` | Object | nVarChar | 20 | [ADP1](ADP1.md) | 4 |  |
| 14 | `RemainDays` | Remaining Life in Days | Num | 19.6 | - |  |  |
| 15 | `TotalUnits` | Total Units in Life | Int | 11 | - |  |  |
| 16 | `RemainUnit` | Remaining Units | Int | 11 | - |  |  |
| 17 | `StanUnit` | Standard Units | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ItemCode, PeriodCat, DprArea |
