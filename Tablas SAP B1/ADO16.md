# ADO16 - Draft - SnB properties

- **Tabla:** ADO16
- **Descripción:** Draft - SnB properties
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ADO16.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Document Number | Int | 11 | [ADOC](ADOC.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `SnBIndex` | SnB Index | Int | 11 | - |  |  |
| 4 | `ItemCode` | Item Code | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 5 | `WhsCode` | Warehouse Code | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 6 | `ObjId` | Object ID | Int | 11 | - |  |  |
| 7 | `ObjAbs` | SnB Object No. | Int | 11 | - |  |  |
| 8 | `DrfWObjAbs` | SnBW Draft Object No. | Int | 11 | - | -1 |  |
| 9 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 10 | `SubLineNum` | Subrow Number | Int | 11 | - | -1 |  |
| 11 | `ObjType` | Object Type | nVarChar | 20 | - |  |  |
| 12 | `LogInstanc` | Log Instance | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineNum, SnBIndex, LogInstanc, ObjType |
