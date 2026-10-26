# OWLBT - Fiori Launchpad Bookmark Tiles

- **Tabla:** OWLBT
- **Descripción:** Fiori Launchpad Bookmark Tiles
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OWLBT.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Guid` | Guid | nVarChar | 40 | - |  |  |
| 2 | `Title` | Title | Text | 16 | - |  |  |
| 3 | `SubTitle` | Sub Title | Text | 16 | - |  |  |
| 4 | `Info` | Icon | Text | 16 | - |  |  |
| 5 | `Bind` | Bind Type | nVarChar | 16 | - |  |  |
| 6 | `Target` | Url Target | Text | 16 | - |  |  |
| 7 | `IsDefault` | Is Default | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `Endpoint` | end point | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Guid |
