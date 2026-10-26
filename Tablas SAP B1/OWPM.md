# OWPM - Process Map

- **Tabla:** OWPM
- **Descripción:** Process Map
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OWPM.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Guid` | GUID of Process Map | nVarChar | 40 | - |  |  |
| 2 | `Name` | Process Map Name | nVarChar | 254 | - |  |  |
| 3 | `IsActive` | Status | VarChar | 1 | - | N | `Y` = Active<br>`N` = Inactive<br>`D` = Draft |
| 4 | `Note` | Note | nVarChar | 254 | - |  |  |
| 5 | `TileEnable` | Display as Tile on Home Page | VarChar | 1 | - | N |  |
| 6 | `IsSystem` | Is System | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 7 | `CreateDate` | Create Date | Date | 8 | - |  |  |
| 8 | `CreateBy` | Create By | Int | 6 | [OUSR](OUSR.md) |  |  |
| 9 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 10 | `UpdateBy` | Update By | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Guid |
