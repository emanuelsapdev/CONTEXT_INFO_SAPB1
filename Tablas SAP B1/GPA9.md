# GPA9 - Applied Gross Profit Adjustments

- **Tabla:** GPA9
- **Descripción:** Applied Gross Profit Adjustments
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/GPA9.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | [OGPA](OGPA.md) |  |  |
| 2 | `LineId` | Row No. | Int | 11 | - |  |  |
| 3 | `DocAbs` | Document Abs. Entry | Int | 11 | - |  |  |
| 4 | `DocType` | Document Type | nVarChar | 20 | - |  |  |
| 5 | `DocLineNum` | Document Line Number | Int | 11 | - |  |  |
| 6 | `SnBAbs` | SnB Abs. Entry | Int | 11 | - |  |  |
| 7 | `ManagedBy` | Managed By | Int | 11 | - | -1 | `10000044` = Batch Numbers<br>`10000045` = Serial Numbers<br>`-1` |
| 8 | `Applied` | Applied Adjustment | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineId |
