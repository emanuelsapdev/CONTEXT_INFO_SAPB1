# UIC5 - Customized Folders in Template

- **Tabla:** UIC5
- **Descripción:** Customized Folders in Template
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/UIC5.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TPLId` | Template ID | Int | 6 | [UICU](UICU.md) |  |  |
| 2 | `FormId` | Form ID | nVarChar | 20 | - |  |  |
| 3 | `ItemId` | Item ID | nVarChar | 20 | - |  |  |
| 4 | `Left` | Left | Int | 6 | - |  |  |
| 5 | `Right` | Right | Int | 6 | - |  |  |
| 6 | `Top` | Top | Int | 6 | - |  |  |
| 7 | `Bottom` | Bottom | Int | 6 | - |  |  |
| 8 | `CurPan` | Current Pane | Int | 6 | - |  |  |
| 9 | `Caption` | Caption | nVarChar | 50 | - |  |  |
| 10 | `GroupItem` | Group Item | nVarChar | 20 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TPLId, FormId, ItemId |
