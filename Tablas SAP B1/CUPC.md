# CUPC - Upgrade Control

- **Tabla:** CUPC
- **Descripción:** Upgrade Control
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CUPC.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ObjectId` | Object ID | nVarChar | 20 | - |  |  |
| 2 | `CntBefore` | Before | Int | 11 | - |  |  |
| 3 | `CntAfter` | After | Int | 11 | - |  |  |
| 4 | `Reported` | Reported | VarChar | 1 | - | O | `C` = Reported<br>`O` = Open |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ObjectId |
