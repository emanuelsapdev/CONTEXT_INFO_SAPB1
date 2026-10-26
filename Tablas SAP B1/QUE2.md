# QUE2 - Queue Elements

- **Tabla:** QUE2
- **Descripción:** Queue Elements
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/QUE2.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `queueID` | Queue ID | nVarChar | 20 | [OQUE](OQUE.md) |  |  |
| 2 | `objType` | Object Type | nVarChar | 20 | - |  |  |
| 3 | `elementId` | Element ID | Int | 11 | - |  |  |
| 4 | `elementNum` | Element Number | Int | 11 | - |  |  |
| 5 | `priority` | Priority | Int | 11 | - |  |  |
| 6 | `createDate` | Creation Date | Date | 8 | - |  |  |
| 7 | `createTime` | Creation Time | Int | 6 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | queueID, elementNum |
| OBJ_ELEM | Yes | queueID, objType, elementId |
