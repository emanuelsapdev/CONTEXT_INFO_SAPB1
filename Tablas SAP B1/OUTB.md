# OUTB - User Tables

- **Tabla:** OUTB
- **Descripción:** User Tables
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OUTB.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TableName` | Table Name | nVarChar | 20 | - |  |  |
| 2 | `Descr` | Description | nVarChar | 30 | - |  |  |
| 3 | `TblNum` | Table number | Int | 11 | - |  |  |
| 4 | `ObjectType` | Object Type | nVarChar | 20 | - | 0 | `0` = No Object<br>`1` = Master Data<br>`2` = Master Data Rows<br>`3` = Document<br>`4` = Document Rows<br>`5` = No Object with Auto. Increment |
| 5 | `UsedInObj` | Used in Object | nVarChar | 20 | - |  |  |
| 6 | `LogTable` | Log Table | nVarChar | 20 | - |  |  |
| 7 | `Archivable` | Archivable | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `ArchivDate` | Archive Date | nVarChar | 18 | - |  |  |
| 9 | `DisplyMenu` | Display Menu | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 10 | `ApplyPerm` | Apply Authorization | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TableName |
