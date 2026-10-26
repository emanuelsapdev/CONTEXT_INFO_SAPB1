# WLPD2 - Fiori Launchpad Tiles

- **Tabla:** WLPD2
- **Descripción:** Fiori Launchpad Tiles
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WLPD2.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `RootId` | Root Guid | nVarChar | 40 | - |  |  |
| 2 | `ParentId` | Parent Id | nVarChar | 40 | - |  |  |
| 3 | `Guid` | Guid | nVarChar | 40 | - |  |  |
| 4 | `Order` | Order | Int | 11 | - |  |  |
| 5 | `TileId` | Tile Id | nVarChar | 40 | - |  |  |
| 6 | `IsDeleted` | Is Deleted | nVarChar | 10 | - | F |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | RootId, ParentId, Guid |
