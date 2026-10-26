# MTBL - MetaData Tables

- **Tabla:** MTBL
- **Descripción:** MetaData Tables
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MTBL.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Name` | Table Name | nVarChar | 5 | - |  |  |
| 2 | `ViewOrder` | View Order | Int | 6 | - | 30 | `-1` = Invisible<br>`10` = Administration<br>`20` = Administration Plus<br>`30` = Master Data<br>`40` = Document Line<br>`50` = Document<br>`60` = Log File<br>`70` = Payment Line<br>`80` = Payments |
| 3 | `Type` | Table Type | Int | 6 | - | 1 | `1` = User OM<br>`2` = User<br>`3` = System OM<br>`4` = System |
| 4 | `Descr` | Description | nVarChar | 254 | - |  |  |
| 5 | `Category` | Category | Int | 6 | - | 0 |  |
| 6 | `SubCateg` | Sub Category | Int | 6 | - | 0 |  |
| 7 | `Dirty` | Dirty | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 8 | `Created` | Creation Date | Date | 8 | - |  |  |
| 9 | `Updated` | Update Date | Date | 8 | - |  |  |
| 10 | `InfoCtgory` | Information Category | Int | 6 | - | 0 |  |
| 11 | `ResCode` | Resource Code from RSBD | Int | 11 | - | -1 |  |
| 12 | `RevCode` | Revision Code | Int | 11 | - | -1 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Name, ResCode, RevCode |
