# MDKY - MetaData Tables DKeys

- **Tabla:** MDKY
- **Descripción:** MetaData Tables DKeys
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MDKY.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TableName` | Table Name | nVarChar | 5 | - |  |  |
| 2 | `HKeyIndex` | HKey Index | Int | 6 | - |  |  |
| 3 | `DKeyIndex` | DKey Index | Int | 6 | - |  |  |
| 4 | `FieldName` | Field in Key | nVarChar | 20 | - |  |  |
| 5 | `Upper` | Upper | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 6 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 7 | `UpdateTime` | Update Time | Int | 11 | - | 0 |  |
| 8 | `UsrSgnAttr` | User Sign For Attribs Change | Int | 11 | - | -1 |  |
| 9 | `ResCode` | Resource Code from RSBD | Int | 11 | - | -1 |  |
| 10 | `RevCode` | Revision Code | Int | 11 | - | -1 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TableName, HKeyIndex, DKeyIndex, ResCode, RevCode |
