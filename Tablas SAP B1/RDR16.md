# RDR16 - Sales Order - SnB properties

- **Tabla:** RDR16
- **Descripción:** Sales Order - SnB properties
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RDR16.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | abs entry | Int | 11 | [ORDR](ORDR.md) |  |  |
| 2 | `LineNum` | Line Number | Int | 11 | - |  |  |
| 3 | `SnBIndex` | SnB Index | Int | 11 | - |  |  |
| 4 | `ItemCode` | Item Code | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 5 | `WhsCode` | Warehouse | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 6 | `ObjId` | Object id | Int | 11 | - |  |  |
| 7 | `ObjAbs` | Object Abs | Int | 11 | - |  |  |
| 8 | `DrfWObjAbs` | draft Wobj Abs | Int | 11 | - | -1 |  |
| 9 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 10 | `SubLineNum` | Subrow Number | Int | 11 | - | -1 |  |
| 11 | `ObjType` | Object Type | nVarChar | 20 | - | 17 |  |
| 12 | `LogInstanc` | Log Instance | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineNum, SnBIndex |
