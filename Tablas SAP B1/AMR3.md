# AMR3 - Inventory Revaluation SNB

- **Tabla:** AMR3
- **Descripción:** Inventory Revaluation SNB
- **Cantidad de campos:** 17
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AMR3.html

## Campos (17)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | - |  |  |
| 2 | `BaseLine` | Base Row Number | Int | 11 | - |  |  |
| 3 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 4 | `SNBNum` | Serial and Batch Number | nVarChar | 36 | - |  |  |
| 5 | `AdmisDate` | Admission Date | Date | 8 | - |  |  |
| 6 | `ExpiryDate` | Expiration Date | Date | 8 | - |  |  |
| 7 | `CurrCost` | Current Cost | Num | 19.6 | - |  |  |
| 8 | `NewCost` | New Cost | Num | 19.6 | - |  |  |
| 9 | `DebCred` | Debit Credit Value | Num | 19.6 | - |  |  |
| 10 | `SNBOpenQty` | SNB Open Quantity | Num | 19.6 | - |  |  |
| 11 | `RToStock` | Reval. Amount Posted to Stock | Num | 19.6 | - |  |  |
| 12 | `SnbSysNum` | SNB System Number | Int | 11 | - |  |  |
| 13 | `SnbAbsEnt` | SNB Abs. Entry | Int | 11 | - |  |  |
| 14 | `SnbQty` | SNB Quantity | Num | 19.6 | - |  |  |
| 15 | `SnbCostT` | SNB Cost Total | Num | 19.6 | - |  |  |
| 16 | `SnbLotNum` | SNB Lot Number | nVarChar | 36 | - |  |  |
| 17 | `SnbMfn` | SNB Manufacture Attribute | nVarChar | 36 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, BaseLine, LineNum |
