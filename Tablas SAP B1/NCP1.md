# NCP1 - New Cockpit Tile

- **Tabla:** NCP1
- **Descripción:** New Cockpit Tile
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/NCP1.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `PageEntry` | Page Number | Int | 11 | - |  |  |
| 3 | `Type` | Type | nVarChar | 20 | - |  |  |
| 4 | `WidgetId` | Widget ID | Int | 11 | - |  |  |
| 5 | `Size` | Size | nVarChar | 10 | - | 1x1 |  |
| 6 | `Index` | Index | Int | 11 | - | 0 |  |
| 7 | `Settings` | Settings | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
