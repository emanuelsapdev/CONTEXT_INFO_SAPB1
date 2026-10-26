# XROBJ - XLR Company Report Objects

- **Tabla:** XROBJ
- **Descripción:** XLR Company Report Objects
- **Cantidad de campos:** 13
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/XROBJ.html

## Campos (13)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `RepObjId` | RepObjId | nVarChar | 38 | - |  |  |
| 2 | `Name` | Name | nVarChar | 50 | - |  |  |
| 3 | `Descriptio` | Description | Text | 16 | - |  |  |
| 4 | `Creator` | Creator | nVarChar | 50 | - |  |  |
| 5 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 6 | `ModifyDate` | ModifyDate | Date | 8 | - |  |  |
| 7 | `ObjType` | ObjType | Int | 11 | - |  |  |
| 8 | `XmlId` | XmlId | nVarChar | 38 | - |  |  |
| 9 | `XlsId` | XlsID | nVarChar | 38 | - |  |  |
| 10 | `VariablesI` | VariablesID | nVarChar | 38 | - |  |  |
| 11 | `Reference` | Reference | Text | 16 | - |  |  |
| 12 | `RefType` | RefType | Int | 11 | - | 0 |  |
| 13 | `Global` | Global | Int | 11 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | RepObjId, Global |
