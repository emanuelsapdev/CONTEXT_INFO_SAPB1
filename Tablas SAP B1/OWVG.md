# OWVG - Variant Groups

- **Tabla:** OWVG
- **Descripción:** Variant Groups
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OWVG.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Guid` | Guid | nVarChar | 40 | - |  |  |
| 2 | `UserId` | User Id | Int | 11 | - |  |  |
| 3 | `ViewType` | View Type | nVarChar | 50 | - |  |  |
| 4 | `ViewId` | View Id | nVarChar | 50 | - | -1 |  |
| 5 | `ObjName` | Object Name | nVarChar | 50 | - |  |  |
| 6 | `DftVrnt` | Default Variant | nVarChar | 40 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Guid |
| GROUP | Yes | UserId, ViewType, ViewId, ObjName |
