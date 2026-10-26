# SXRDF - XLR Definition

- **Tabla:** SXRDF
- **Descripción:** XLR Definition
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SXRDF.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DimFilterI` | DimFilterId | Identity | 11 | - |  |  |
| 2 | `RoleId` | RoleId | nVarChar | 16 | - |  |  |
| 3 | `DimId` | DimId | nVarChar | 20 | - |  |  |
| 4 | `ModuleId` | ModuleId | nVarChar | 20 | - |  |  |
| 5 | `AccessType` | AccessType | Int | 11 | - | 0 |  |
| 6 | `ReadInclud` | ReadIncludeExpr | Text | 16 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DimFilterI |
| second | Yes | RoleId, DimId |
