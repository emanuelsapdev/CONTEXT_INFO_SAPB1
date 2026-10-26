# OCMN - Customized Menu

- **Tabla:** OCMN
- **Descripción:** Customized Menu
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCMN.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `GUID` | GUID | nVarChar | 32 | - |  |  |
| 2 | `Name` | Menu Item Name | nVarChar | 100 | - |  |  |
| 3 | `Father` | Menu Parent GUID | nVarChar | 32 | - |  |  |
| 4 | `Type` | Menu Type | VarChar | 1 | - | C | `S`<br>`A`<br>`C` |
| 5 | `SubMenu` | Submenu Flag | VarChar | 1 | - | N | `Y`<br>`N` |
| 6 | `MenuUID` | Menu UID | nVarChar | 50 | - |  |  |
| 7 | `ObjectType` | Target Object Type | Int | 11 | - |  |  |
| 8 | `ObjectKey` | Target Object ID | nVarChar | 200 | - |  |  |
| 9 | `PermFolder` | Permission Folder ID | Int | 11 | - |  |  |
| 10 | `SortOrder` | Sort Order | Int | 11 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | GUID |
| UID_KEY | No | MenuUID |
