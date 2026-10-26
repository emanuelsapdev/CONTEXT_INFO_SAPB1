# EESUB - EESUB

- **Tabla:** EESUB
- **Descripción:** EESUB
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/EESUB.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `EventType` |  | nVarChar | 30 | - |  |  |
| 2 | `Processor` |  | nVarChar | 60 | - |  |  |
| 3 | `ReceiverId` |  | nVarChar | 50 | - |  |  |
| 4 | `ReturnAddr` |  | nVarChar | 254 | - |  |  |
| 5 | `SenderId` |  | nVarChar | 50 | - |  |  |
| 6 | `FilterName` |  | nVarChar | 60 | - |  |  |
| 7 | `FilterVal` |  | nVarChar | 60 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | EventType, Processor, ReturnAddr, ReceiverId, SenderId |
