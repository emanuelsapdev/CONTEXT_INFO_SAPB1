# MIDX - MIDX

- **Tabla:** MIDX
- **Descripción:** MIDX
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MIDX.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `guid` |  | nVarChar | 36 | - |  |  |
| 2 | `fatherId` |  | nVarChar | 36 | - |  |  |
| 3 | `idxName` |  | nVarChar | 36 | - |  |  |
| 4 | `isUnique` |  | VarChar | 1 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | fatherId, idxName |
| GUID | Yes | guid |
