# UWOR3 - Production Order - Closure

- **Tabla:** UWOR3
- **Descripción:** Production Order - Closure
- **Cantidad de campos:** 13
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/UWOR3.html

## Campos (13)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal Number | Int | 11 | - |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `LayerID` | Layer ID | Int | 11 | - |  |  |
| 4 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 5 | `RToStock` | Reval. Amount Posted to Stock | Num | 19.6 | - |  |  |
| 6 | `RToStockSc` | Reval. Amt Posted to Stock SC | Num | 19.6 | - |  |  |
| 7 | `WhsCode` | Warehouse Code | nVarChar | 8 | - |  |  |
| 8 | `IVLTransSe` | IVL Transaction Sequence No. | Int | 11 | - |  |  |
| 9 | `IVLLayerID` | IVL Layer ID | Int | 11 | - |  |  |
| 10 | `SnbSysNum` | SNB System Number | Int | 11 | - |  |  |
| 11 | `SnbAbsEnt` | SNB Abs. Entry | Int | 11 | - |  |  |
| 12 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 13 | `INMSubLine` | INM Subrow Number | Int | 11 | - | -1 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum, LayerID |
