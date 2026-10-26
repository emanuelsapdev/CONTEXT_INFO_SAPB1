# ODPV - Fixed Assets Depreciation Value

- **Tabla:** ODPV
- **Descripción:** Fixed Assets Depreciation Value
- **Cantidad de campos:** 17
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ODPV.html

## Campos (17)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `ItemCode` | Item Code | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 3 | `DprArea` | Depreciation Area ID | nVarChar | 15 | [ODPA](ODPA.md) |  |  |
| 4 | `PeriodCat` | Period Category | nVarChar | 10 | - |  |  |
| 5 | `FromDate` | Period Start Date | Date | 8 | - |  |  |
| 6 | `ToDate` | Period To Date | Date | 8 | - |  |  |
| 7 | `OrdDprPlan` | Ordinary Depreciation Plan | Num | 19.6 | - |  |  |
| 8 | `OrdDprPost` | Ordinary Depreciation Posted | Num | 19.6 | - |  |  |
| 9 | `OrdDprAct` | Ordinary Depreciation Actual | Num | 19.6 | - |  |  |
| 10 | `SpDprKey` | Special Depreciation Key | nVarChar | 2 | [ODPP](ODPP.md) |  |  |
| 11 | `SpDprPlan` | Special Depreciation Plan | Num | 19.6 | - |  |  |
| 12 | `SpDprPost` | Special Depreciation Posted | Num | 19.6 | - |  |  |
| 13 | `SpDprAct` | Special Depreciation Actual | Num | 19.6 | - |  |  |
| 14 | `SubPeriod` | Sub-period | Int | 11 | - |  |  |
| 15 | `OrdDprPln1` | Ordinary Depreciation Plan 1 | Num | 19.6 | - |  |  |
| 16 | `OrdDprPst1` | Ordinary Depreciation Posted 1 | Num | 19.6 | - |  |  |
| 17 | `OrdDprAct1` | Ordinary Depreciation Actual 1 | Num | 19.6 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| SECONDARY | Yes | ItemCode, DprArea, PeriodCat, SubPeriod |
