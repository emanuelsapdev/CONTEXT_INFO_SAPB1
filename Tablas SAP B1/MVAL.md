# MVAL - MetaData Tables Fields Vals

- **Tabla:** MVAL
- **Descripción:** MetaData Tables Fields Vals
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MVAL.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TableName` | Table Name | nVarChar | 5 | - |  |  |
| 2 | `FieldIndex` | Field Index | Int | 6 | - |  |  |
| 3 | `ValIndex` | Val Index | Int | 6 | - |  |  |
| 4 | `Value` | Value | nVarChar | 254 | - |  |  |
| 5 | `Descr` | Description | nVarChar | 254 | - |  |  |
| 6 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 7 | `UpdateTime` | Update Time | Int | 11 | - | 0 |  |
| 8 | `UsrSgnAttr` | User Sign For Attribs Change | Int | 11 | - | -1 |  |
| 9 | `DiEnumCode` | DI Enum Code | Int | 11 | - |  |  |
| 10 | `DiEnItCode` | DI Enum Item Code | Int | 11 | - |  |  |
| 11 | `ResCode` | Resource Code from RSBD | Int | 11 | - | -1 |  |
| 12 | `RevCode` | Revision Code | Int | 11 | - | -1 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TableName, FieldIndex, ValIndex, ResCode, RevCode |
