# SDRF - Drag&Relate - Files

- **Tabla:** SDRF
- **Descripción:** Drag&Relate - Files
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SDRF.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ObjectId` | ObjectId | nVarChar | 4 | - |  |  |
| 2 | `DescStr` | Description | nVarChar | 30 | - |  |  |
| 3 | `FatherId` | FatherId | nVarChar | 4 | - |  |  |
| 4 | `VisLevel` | Visual level | Int | 6 | - |  | `1`<br>`2` |
| 5 | `VisOrder` | Visual order | Int | 6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ObjectId |
