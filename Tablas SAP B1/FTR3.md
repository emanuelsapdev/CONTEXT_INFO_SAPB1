# FTR3 - Transfer - Item Areas

- **Tabla:** FTR3
- **Descripción:** Transfer - Item Areas
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/FTR3.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | [OACQ](OACQ.md) |  |  |
| 2 | `ItemLine` | Item Row Number | Int | 11 | - |  |  |
| 3 | `ItemCode` | Item Code | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 4 | `DprArea` | Depreciation Area | nVarChar | 15 | [ODPA](ODPA.md) |  |  |
| 5 | `Total` | Total | Num | 19.6 | - |  |  |
| 6 | `TotalFrgn` | Total (FC) | Num | 19.6 | - |  |  |
| 7 | `TotalSys` | Total (SC) | Num | 19.6 | - |  |  |
| 8 | `ObjType` | Object Type | nVarChar | 20 | - |  |  |
| 9 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, ItemLine, DprArea |
