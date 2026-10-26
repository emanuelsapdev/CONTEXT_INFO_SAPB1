# MFLD - MetaData Tables Fields

- **Tabla:** MFLD
- **Descripción:** MetaData Tables Fields
- **Cantidad de campos:** 27
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MFLD.html

## Campos (27)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TableName` | Table Name | nVarChar | 5 | - |  |  |
| 2 | `FieldIndex` | Field Index | Int | 6 | - |  |  |
| 3 | `Name` | Field Name | nVarChar | 20 | - |  |  |
| 4 | `Alias` | Alias | nVarChar | 10 | - |  |  |
| 5 | `Descr` | Description | nVarChar | 250 | - |  |  |
| 6 | `Type` | Type | VarChar | 1 | - | A | `A` = DB Alpha<br>`M` = DB Memo<br>`N` = DB Numeric<br>`D` = DB Date<br>`B` = DB Binary<br>`I` = DB Auto Key |
| 7 | `Size` | Size | Int | 6 | - |  |  |
| 8 | `FieldType` | Field Type Num | Int | 6 | - |  |  |
| 9 | `Visible` | Visible | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 10 | `EditType` | Edit Type | VarChar | 1 | - |  |  |
| 11 | `EditSize` | Edit Size | Int | 6 | - |  |  |
| 12 | `RFile` | Related Table | nVarChar | 4 | - |  |  |
| 13 | `ColHeading` | Column Heading | nVarChar | 30 | - |  |  |
| 14 | `FrmHeading` | Form Heading | nVarChar | 30 | - |  |  |
| 15 | `GroupNum` | Group Number | Int | 6 | - | 0 | `0` = User<br>`-1` = System |
| 16 | `DefaultVal` | Default Value | nVarChar | 254 | - |  |  |
| 17 | `DIStatus` | DI Status | VarChar | 1 | - | E | `N` = Not added to DI<br>`Y` = Added as Read/Write<br>`R` = Added as Read Only<br>`E` = NOT DEFINED |
| 18 | `Dirty` | Dirty | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 19 | `Flag1` | Flag1 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 20 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 21 | `UpdateTime` | Update Time | Int | 11 | - | 0 |  |
| 22 | `UsrSgnAttr` | User Sign For Attribs Change | Int | 11 | - | -1 |  |
| 23 | `ResCode` | Resource Code from RSBD | Int | 11 | - | -1 |  |
| 24 | `RevCode` | Revision Code | Int | 11 | - | -1 |  |
| 25 | `AssGrp` | Association Group | nVarChar | 16 | - |  |  |
| 26 | `AssType` | Association Type | nVarChar | 2 | - | -1 | `-1`<br>`OT` = Object Type<br>`O1` = Object Key Seg. 1<br>`O2` = Object Key Seg. 2<br>`O3` = Object Key Seg. 3<br>`O4` = Object Key Seg. 4<br>`O5` = Object Key Seg. 5<br>`O6` = Object Key Seg. 6<br>`AO` = Array Offset<br>`A1` = Array Key 1<br>`A2` = Array Key 2<br>`A3` = Array Key 3 |
| 27 | `IsPersist` | Is Field Persistant | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TableName, FieldIndex, ResCode, RevCode |
