# CIGR - Approval Process Ignore List

- **Tabla:** CIGR
- **Descripción:** Approval Process Ignore List
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CIGR.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Category` | Category | VarChar | 1 | - |  | `D` = Document<br>`O` = Inventory Opening Balance<br>`P` = Inventory Posting<br>`C` = Inventory Counting<br>`V` = Payment |
| 2 | `TableName` | Table Name | nVarChar | 20 | - |  |  |
| 3 | `FieldName` | Field Name | nVarChar | 50 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TableName, FieldName |
