# SDRQ - Drag&Relate - Queries

- **Tabla:** SDRQ
- **Descripción:** Drag&Relate - Queries
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SDRQ.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ObjTo` | ObjectTo | nVarChar | 4 | - |  |  |
| 2 | `ObjFrom` | ObjectFrom | nVarChar | 4 | - |  |  |
| 3 | `JoinStr` | Join String | nVarChar | 254 | - |  |  |
| 4 | `FilterStr` | Filter String | nVarChar | 128 | - |  |  |
| 5 | `ServerType` | Server Type | Int | 11 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ObjTo, ObjFrom, ServerType |
