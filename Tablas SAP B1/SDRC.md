# SDRC - Drag&Relate - Categories

- **Tabla:** SDRC
- **Descripción:** Drag&Relate - Categories
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SDRC.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ObjectId` | ObjectId | nVarChar | 4 | - |  |  |
| 2 | `DescStr` | Description | nVarChar | 30 | - |  |  |
| 3 | `VisOrder` | Visual order | Int | 6 | - |  |  |
| 4 | `PartOf` | PartOf | VarChar | 1 | - | D | `D` = Docs<br>`R` = Reports<br>`T` = Tools |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ObjectId |
