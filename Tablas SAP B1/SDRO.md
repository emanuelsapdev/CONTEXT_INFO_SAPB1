# SDRO - Drag&Relate - Output fields

- **Tabla:** SDRO
- **Descripción:** Drag&Relate - Output fields
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SDRO.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ObjectId` | Object Id | nVarChar | 4 | - |  |  |
| 2 | `FieldId` | Field Id | Int | 6 | - |  |  |
| 3 | `DescStr` | Description | nVarChar | 30 | - |  |  |
| 4 | `VisOrder` | Visual order | Int | 6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ObjectId, FieldId |
