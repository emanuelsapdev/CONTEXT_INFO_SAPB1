# OIRC - Interactive Report Category

- **Tabla:** OIRC
- **Descripción:** Interactive Report Category
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OIRC.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CategoryId` | Category Id | Int | 11 | - |  |  |
| 2 | `ParentId` | Parent Category Id | Int | 11 | - | -1 |  |
| 3 | `Name` | Category Name | nVarChar | 254 | - |  |  |
| 4 | `ResKey` | Resource Key | nVarChar | 128 | - |  |  |
| 5 | `Comment` | Comment | nVarChar | 254 | - |  |  |
| 6 | `System` | System | VarChar | 1 | - | N |  |
| 7 | `CreateBy` | Created By | nVarChar | 25 | - |  |  |
| 8 | `CreateDate` | Creation Timestamp | Date | 8 | - |  |  |
| 9 | `ModifyBy` | Modified By | nVarChar | 25 | - |  |  |
| 10 | `ModifyDate` | Modification Timestamp | Date | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CategoryId |
