# NCP2 - New Cockpit Tile

- **Tabla:** NCP2
- **Descripción:** New Cockpit Tile
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/NCP2.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `PageEntry` | Page Number | Int | 11 | [ONCP](ONCP.md) |  |  |
| 2 | `Type` | Type | nVarChar | 20 | [NCP1](NCP1.md) |  |  |
| 3 | `ObjectType` | Object Type | Int | 11 | [CDPM](CDPM.md) |  |  |
| 4 | `ObjectKey` | Object ID | nVarChar | 50 | [CDPM](CDPM.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | PageEntry, ObjectType, ObjectKey |
