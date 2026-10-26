# WORF - Object Wizard Related Files

- **Tabla:** WORF
- **Descripción:** Object Wizard Related Files
- **Cantidad de campos:** 16
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WORF.html

## Campos (16)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ObjName` | Parent Object Code | Int | 11 | - |  |  |
| 2 | `SonNum` | Son Number | Int | 11 | - |  |  |
| 3 | `ObjTable` | Son Table | nVarChar | 20 | - |  |  |
| 4 | `RelObj` | Object | nVarChar | 20 | - |  |  |
| 5 | `RelType` | Relationship Type | VarChar | 1 | - | L | `L` = Line<br>`O` = Odd<br>`A` = Another object contained |
| 6 | `LogSon` | Son's Log table | nVarChar | 20 | - |  |  |
| 7 | `FthrLineId` | Father's Line Id | Int | 11 | - | 0 |  |
| 8 | `UniqueId` | Son Unique Id | Int | 11 | - |  |  |
| 9 | `LnObjCode` | Line object code | nVarChar | 20 | - |  |  |
| 10 | `SonDesc` | Son Description | nVarChar | 30 | - |  |  |
| 11 | `CreateDate` | Creation date | Date | 8 | - |  |  |
| 12 | `CreateTime` | Creation Time | Int | 6 | - |  |  |
| 13 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 14 | `UpdateTime` | Update Time | Int | 6 | - |  |  |
| 15 | `UserSign` | User Sign | Int | 11 | - |  |  |
| 16 | `FieldIndex` | Field Index | Int | 6 | - |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ObjName, SonNum |
| UNIQUE_ID | Yes | UniqueId |
| TABLE | Yes | ObjName, ObjTable |
