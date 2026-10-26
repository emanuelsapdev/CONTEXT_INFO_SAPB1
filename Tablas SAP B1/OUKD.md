# OUKD - User Key Description

- **Tabla:** OUKD
- **Descripción:** User Key Description
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OUKD.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TableName` | Table Name | nVarChar | 20 | - |  |  |
| 2 | `KeyId` | Key Index | Int | 6 | - |  |  |
| 3 | `KeyName` | Key Name | nVarChar | 10 | - |  |  |
| 4 | `UniqueKey` | Unique Key | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 5 | `Action` | Action | VarChar | 1 | - | N | `A` = Add<br>`U` = Update<br>`D` = Delete<br>`N` = None |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TableName, KeyId |
