# ITM8 - Asset Item Balances

- **Tabla:** ITM8
- **Descripción:** Asset Item Balances
- **Cantidad de campos:** 21
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ITM8.html

## Campos (21)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 2 | `PeriodCat` | Period Category | nVarChar | 10 | - |  |  |
| 3 | `DprArea` | Depreciation Area | nVarChar | 15 | [ODPA](ODPA.md) |  |  |
| 4 | `APC` | APC | Num | 19.6 | - |  |  |
| 5 | `APCHist` | Historical APC | Num | 19.6 | - |  |  |
| 6 | `Quantity` | Asset Quantity | Num | 19.6 | - |  |  |
| 7 | `OrDpAcc` | Accumulated Ordinary Depr. | Num | 19.6 | - |  |  |
| 8 | `UnDpAcc` | Accumulated Unplanned Depr. | Num | 19.6 | - |  |  |
| 9 | `SpDpKey1` | Special Depreciation 01 | nVarChar | 2 | [ODPP](ODPP.md) |  |  |
| 10 | `SpDpAcc1` | Accumulated Special Depr. 01 | Num | 19.6 | - |  |  |
| 11 | `SpDpKey2` | Special Depreciation 02 | nVarChar | 2 | [ODPP](ODPP.md) |  |  |
| 12 | `SpDpAcc2` | Accumulated Special Depr. 02 | Num | 19.6 | - |  |  |
| 13 | `SpDpKey3` | Special Depreciation 03 | nVarChar | 2 | [ODPP](ODPP.md) |  |  |
| 14 | `SpDpAcc3` | Accumulated Special Depr. 03 | Num | 19.6 | - |  |  |
| 15 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 16 | `ObjType` | Object | nVarChar | 20 | [ADP1](ADP1.md) | 4 |  |
| 17 | `SalvageVal` | Salvage Value | Num | 19.6 | - |  |  |
| 18 | `OrDpAcc1` | Ordinary Depr. Accumulation 01 | Num | 19.6 | - |  |  |
| 19 | `WriteUpAcc` | Accumulated Write-Up | Num | 19.6 | - |  |  |
| 20 | `IsMaSalVal` | Manually Changed Salvage Value | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 21 | `AppreAcc` | Accumulated Appreciation | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ItemCode, PeriodCat, DprArea |
