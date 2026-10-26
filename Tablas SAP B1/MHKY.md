# MHKY - MetaData Tables HKeys

- **Tabla:** MHKY
- **Descripción:** MetaData Tables HKeys
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MHKY.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TableName` | Table Name | nVarChar | 5 | - |  |  |
| 2 | `HKeyIndex` | HKey Index | Int | 6 | - |  |  |
| 3 | `Name` | Key Name | nVarChar | 10 | - |  |  |
| 4 | `ViewOrder` | View Order | Int | 6 | - |  |  |
| 5 | `UniqueKey` | Unique Key | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 6 | `Ascend` | Ascending | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 7 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 8 | `UpdateTime` | Update Time | Int | 11 | - | 0 |  |
| 9 | `UsrSgnAttr` | User Sign For Attribs Change | Int | 11 | - | -1 |  |
| 10 | `ResCode` | Resource Code from RSBD | Int | 11 | - | -1 |  |
| 11 | `RevCode` | Revision Code | Int | 11 | - | -1 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TableName, HKeyIndex, ResCode, RevCode |
