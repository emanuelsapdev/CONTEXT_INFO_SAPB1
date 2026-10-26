# ADO10 - Marketing Document - Row Structure - History

- **Tabla:** ADO10
- **Descripción:** Marketing Document - Row Structure - History
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ADO10.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | [ADOC](ADOC.md) |  |  |
| 2 | `LineSeq` | Row Sequence | Int | 11 | - |  |  |
| 3 | `AftLineNum` | After Row Number | Int | 11 | - |  |  |
| 4 | `OrderNum` | Order Number | Int | 11 | - |  |  |
| 5 | `LineType` | Row Type | VarChar | 1 | - |  | `T` = Text<br>`S` = Subtotal |
| 6 | `LineText` | Row Text | Text | 16 | - |  |  |
| 7 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 8 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 23 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineSeq, ObjType, LogInstanc |
