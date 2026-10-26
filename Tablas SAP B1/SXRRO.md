# SXRRO - XLR Relations

- **Tabla:** SXRRO
- **Descripción:** XLR Relations
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SXRRO.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `RoleId` | RoleId | nVarChar | 16 | - |  |  |
| 2 | `AppId` | AppId | nVarChar | 225 | - |  |  |
| 3 | `DatabaseId` | DatabaseId | nVarChar | 225 | - |  |  |
| 4 | `Name` | Name | nVarChar | 50 | - |  |  |
| 5 | `Descriptio` | Description | nVarChar | 254 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | RoleId |
| second | Yes | AppId, DatabaseId, Name |
