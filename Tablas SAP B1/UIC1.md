# UIC1 - Customized Forms in Templates

- **Tabla:** UIC1
- **Descripción:** Customized Forms in Templates
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/UIC1.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TPLId` | Template ID | Int | 6 | [UICU](UICU.md) |  |  |
| 2 | `FormId` | Form ID | nVarChar | 20 | - |  |  |
| 3 | `Width` | Form Width | Int | 6 | - |  |  |
| 4 | `Height` | Form Height | Int | 6 | - |  |  |
| 5 | `MenuId` | Menu ID | nVarChar | 20 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TPLId, FormId |
