# MKEY - MKEY

- **Tabla:** MKEY
- **Descripción:** MKEY
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MKEY.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `guid` | Unique Id | nVarChar | 36 | - |  |  |
| 2 | `fatherId` | Meta Object Guid | nVarChar | 36 | - |  |  |
| 3 | `columnId` | Column Id | nVarChar | 36 | - |  |  |
| 4 | `lineNum` | Line Number | Int | 11 | - |  |  |
| 5 | `fatheColId` | Father Column Id | nVarChar | 36 | - |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | fatherId, lineNum |
| GUID | Yes | guid |
| COLUMN | Yes | fatherId, columnId |
