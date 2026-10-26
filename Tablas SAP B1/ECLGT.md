# ECLGT - ECLGT

- **Tabla:** ECLGT
- **Descripción:** ECLGT
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ECLGT.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Id` | transaction id | nVarChar | 100 | - |  |  |
| 2 | `TableName` | db table name | nVarChar | 50 | - |  |  |
| 3 | `TableId` | id field within db table | nVarChar | 100 | - |  |  |
| 4 | `CfgCol` | column within db table | nVarChar | 50 | - |  |  |
| 5 | `OldValue` |  | nVarChar | 254 | - |  |  |
| 6 | `NewValue` |  | nVarChar | 254 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Id, TableName, TableId, CfgCol |
