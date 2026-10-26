# UIC2 - Customized Forms in Template

- **Tabla:** UIC2
- **Descripción:** Customized Forms in Template
- **Cantidad de campos:** 15
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/UIC2.html

## Campos (15)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TPLId` | Template ID | Int | 6 | [UICU](UICU.md) |  |  |
| 2 | `FormId` | Form ID | nVarChar | 20 | - |  |  |
| 3 | `ItemId` | Item ID | nVarChar | 70 | - |  |  |
| 4 | `Visible` | Visible | VarChar | 1 | - |  |  |
| 5 | `VisibleCtl` | Visible Control | VarChar | 1 | - |  |  |
| 6 | `Editable` | Editable | VarChar | 1 | - |  |  |
| 7 | `EditbleCtl` | Editable Control | VarChar | 1 | - |  |  |
| 8 | `Left` | Left | Int | 6 | - |  |  |
| 9 | `Top` | Top | Int | 6 | - |  |  |
| 10 | `Right` | Right | Int | 6 | - |  |  |
| 11 | `Bottom` | Bottom | Int | 6 | - |  |  |
| 12 | `FromPane` | From Pane | Int | 6 | - |  |  |
| 13 | `ToPane` | To Pane | Int | 6 | - |  |  |
| 14 | `UDF` | UDF | VarChar | 1 | - | N |  |
| 15 | `TableName` | TableName | nVarChar | 20 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TPLId, FormId, ItemId |
