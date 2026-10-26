# GFL1 - Grid Filter Rules

- **Tabla:** GFL1
- **Descripción:** Grid Filter Rules
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/GFL1.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `FormID` | Form ID | nVarChar | 20 | - |  |  |
| 2 | `GridID` | Grid ID | nVarChar | 11 | - |  |  |
| 3 | `UserCode` | User Code | Int | 6 | - |  |  |
| 4 | `FilterID` | Filter ID | Int | 11 | - |  |  |
| 5 | `GridColumn` | Grid Column | Int | 6 | - |  |  |
| 6 | `FilterRule` | FilterRule | Int | 6 | - |  |  |
| 7 | `Value` | Value | nVarChar | 254 | - |  |  |
| 8 | `ValueTo` | ValueTo | nVarChar | 254 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | FormID, GridID, UserCode, FilterID, GridColumn |
