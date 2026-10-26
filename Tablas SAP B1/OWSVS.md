# OWSVS - Web Client Linked View Sequence

- **Tabla:** OWSVS
- **Descripción:** Web Client Linked View Sequence
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OWSVS.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `SeqId` | Sequence ID | nVarChar | 40 | - |  |  |
| 2 | `ObjType` | Object Type | nVarChar | 32 | - |  |  |
| 3 | `UserId` | User ID | Int | 11 | - |  |  |
| 4 | `ViewType` | Type of Linked View | nVarChar | 20 | - | DetailedViewHeader | `ListView` = List View<br>`DetailedViewHeader` = Detailed View Header<br>`DetailedViewRows` = Detailed View Rows |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | SeqId |
