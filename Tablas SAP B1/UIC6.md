# UIC6 - Template Group Customization

- **Tabla:** UIC6
- **Descripción:** Template Group Customization
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/UIC6.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TPLId` | Template ID | Int | 6 | [UICU](UICU.md) |  |  |
| 2 | `GroupID` | Group ID | Int | 6 | [OUGR](OUGR.md) |  |  |
| 3 | `IsTemplate` | Is Template | VarChar | 1 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TPLId, GroupID |
