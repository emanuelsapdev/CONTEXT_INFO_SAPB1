# SXRSS - XLR Security Settings

- **Tabla:** SXRSS
- **Descripción:** XLR Security Settings
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SXRSS.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `SecuritySe` | SecuritySettingId | Identity | 11 | - |  |  |
| 2 | `AppId` | AppId | nVarChar | 218 | - |  |  |
| 3 | `DatabaseId` | DatabaseId | nVarChar | 218 | - |  |  |
| 4 | `ModuleId` | ModuleId | nVarChar | 20 | - | '' | `''` |
| 5 | `Label` | Label | nVarChar | 50 | - |  |  |
| 6 | `Value` | Value | Text | 16 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | SecuritySe |
| second | Yes | AppId, DatabaseId, ModuleId, Label |
