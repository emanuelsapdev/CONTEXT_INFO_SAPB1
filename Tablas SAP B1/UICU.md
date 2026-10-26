# UICU - Customized Template

- **Tabla:** UICU
- **Descripción:** Customized Template
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/UICU.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TPLId` | Template ID | Int | 6 | - |  |  |
| 2 | `TPLName` | Template Name | nVarChar | 155 | - |  |  |
| 3 | `TPLDesc` | Template Description | nVarChar | 155 | - |  |  |
| 4 | `UserID` | User ID | Int | 6 | - |  |  |
| 5 | `Parent` | Parent Template ID | Int | 6 | - |  |  |
| 6 | `IsTemplate` | Is Template | VarChar | 1 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TPLId |
| NAME_KEY | Yes | TPLName |
