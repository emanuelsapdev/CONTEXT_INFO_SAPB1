# AQI2 - Inventory Opening Balance - SnB

- **Tabla:** AQI2
- **Descripción:** Inventory Opening Balance - SnB
- **Cantidad de campos:** 13
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AQI2.html

## Campos (13)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Number | Int | 11 | [OINC](OINC.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `SnbIndex` | SnB Index | Int | 11 | - |  |  |
| 4 | `ItemCode` | Item Code | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 5 | `WhsCode` | Warehouse | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 6 | `ObjId` | Object ID | Int | 11 | - |  |  |
| 7 | `ObjAbs` | Object Abs. | Int | 11 | - |  |  |
| 8 | `DrfWObjAbs` | Draft Whse Obj. Abs. | Int | 11 | - | -1 |  |
| 9 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 10 | `SubLineNum` | Subrow Number | Int | 11 | - | -1 |  |
| 11 | `ObjType` | Object Type | nVarChar | 20 | - |  |  |
| 12 | `LogInstanc` | Log Instance - History | Int | 11 | - |  |  |
| 13 | `TakerType` | Counter Type | Int | 11 | - |  | `0` = One Counter<br>`1` = Two Counters - Counter 1<br>`2` = Two Counters - Counter 2 |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum, SnbIndex, LogInstanc |
