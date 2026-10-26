# UKD1 - User Sub-Keys Description

- **Tabla:** UKD1
- **Descripción:** User Sub-Keys Description
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/UKD1.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TableName` | Table Name | nVarChar | 20 | - |  |  |
| 2 | `KeyId` | Key Index | Int | 6 | - |  |  |
| 3 | `SubKeyId` | Sub-Key Index | Int | 6 | - |  |  |
| 4 | `ColAlias` | Column Alias | nVarChar | 50 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TableName, KeyId, SubKeyId |
| ALIAS | No | TableName, ColAlias |
