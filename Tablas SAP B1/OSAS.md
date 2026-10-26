# OSAS - Sales App Setting

- **Tabla:** OSAS
- **Descripción:** Sales App Setting
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSAS.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Code | Int | 11 | - |  |  |
| 2 | `Name` | Name | nVarChar | 100 | - |  |  |
| 3 | `AdBoardId` | Advanced Dashboard ID | Int | 11 | [OXAP](OXAP.md) |  |  |
| 4 | `CAdBoardId` | Customer Advanced Dashboard ID | Int | 11 | [OXAP](OXAP.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code |
