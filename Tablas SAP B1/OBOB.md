# OBOB - Business Object Brief

- **Tabla:** OBOB
- **Descripción:** Business Object Brief
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OBOB.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ObjectId` | Object ID | Int | 11 | - |  |  |
| 2 | `TableName` | Table Name | nVarChar | 30 | - |  |  |
| 3 | `PrimaryKey` | Primary Key | nVarChar | 30 | - |  |  |
| 4 | `TitleField` | Title Field | nVarChar | 100 | - |  |  |
| 5 | `DescField` | Description Field | nVarChar | 100 | - |  |  |
| 6 | `DeviceType` | Device Type | VarChar | 1 | - | D | `D` = Desktop<br>`M` = Mobile |
| 7 | `UsedBy` | The record is used by BO list/Quick Access/Both | VarChar | 1 | - | A | `A` = All<br>`B` = BO List<br>`R` = Recent Updates |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ObjectId |
