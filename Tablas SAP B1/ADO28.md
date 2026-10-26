# ADO28 - Marketing Document - Reported Tracking Note - History

- **Tabla:** ADO28
- **Descripción:** Marketing Document - Reported Tracking Note - History
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ADO28.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | ODOC |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `ChildNum` | Assignment Line | Int | 11 | - |  |  |
| 4 | `TrackingNt` | CCD Tracking Note | Int | 11 | [OTCN](OTCN.md) |  |  |
| 5 | `TrackiNtLn` | CCD Tracking Note Line | Int | 11 | - |  |  |
| 6 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 7 | `UnusedQty` | Unused Quantity | Num | 19.6 | - |  |  |
| 8 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 9 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 0 |  |
| 10 | `SubLineNum` | BOM Line No. | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum, ChildNum, LogInstanc, ObjType |
