# UIC4 - Forms in Assigned Templates

- **Tabla:** UIC4
- **Descripción:** Forms in Assigned Templates
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/UIC4.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TPLId` | Template ID | Int | 6 | [UICU](UICU.md) |  |  |
| 2 | `FormId` | Form ID | nVarChar | 20 | - |  |  |
| 3 | `UserID` | User ID | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | UserID, FormId, TPLId |
