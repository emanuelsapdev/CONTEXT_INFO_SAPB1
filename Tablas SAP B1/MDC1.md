# MDC1 - Master Data Cleanup - Log

- **Tabla:** MDC1
- **Descripción:** Master Data Cleanup - Log
- **Cantidad de campos:** 15
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MDC1.html

## Campos (15)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | [OMDC](OMDC.md) |  |  |
| 2 | `LineID` | Line ID | Int | 11 | - |  |  |
| 3 | `ObjectType` | Object Type | nVarChar | 20 | - |  |  |
| 4 | `ObjectKey` | Object Key | nVarChar | 20 | - |  |  |
| 5 | `Name` | Name | nVarChar | 200 | - |  |  |
| 6 | `LastDate` | Last Transaction Date | Date | 8 | - |  |  |
| 7 | `Action` | Action | VarChar | 1 | - |  | `R` = Remove<br>`D` = Deactivate |
| 8 | `ObjectCode` | Object Code | nVarChar | 100 | - |  |  |
| 9 | `ActFailed` | Action Failed | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 10 | `OrigAction` | Original Action | VarChar | 1 | - |  | `R` = Remove<br>`D` = Deactivate |
| 11 | `SubObjType` | Subobject Type | nVarChar | 20 | - |  |  |
| 12 | `SubObjKey` | Subobject Key | nVarChar | 50 | - |  |  |
| 13 | `SubObjNam1` | Subobject Name 1 | nVarChar | 50 | - |  |  |
| 14 | `SubObjNam2` | Subobject Name 2 | nVarChar | 50 | - |  |  |
| 15 | `SubObjNam3` | Subobject Name 3 | nVarChar | 50 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineID |
