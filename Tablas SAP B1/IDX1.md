# IDX1 - IDX1

- **Tabla:** IDX1
- **Descripción:** IDX1
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/IDX1.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `guid` |  | nVarChar | 36 | - |  |  |
| 2 | `fatherId` |  | nVarChar | 36 | - |  |  |
| 3 | `columnId` |  | nVarChar | 36 | - |  |  |
| 4 | `lineNum` |  | Int | 11 | - |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | fatherId, lineNum |
| GUID | Yes | guid |
| COLUMN | Yes | fatherId, columnId |
