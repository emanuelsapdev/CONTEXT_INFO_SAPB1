# XRREL - XLR Company Report Objects

- **Tabla:** XRREL
- **Descripción:** XLR Company Report Objects
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/XRREL.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ParentId` | ParentId | nVarChar | 38 | - |  |  |
| 2 | `ChildId` | ChildId | nVarChar | 38 | - |  |  |
| 3 | `RelType` | RelType | Int | 11 | - | 1 |  |
| 4 | `SeqNo` | SeqNo | Int | 11 | - | 0 |  |
| 5 | `Global` | Global | Int | 11 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ParentId, ChildId, Global |
