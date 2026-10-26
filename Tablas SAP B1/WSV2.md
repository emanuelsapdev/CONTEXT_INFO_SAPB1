# WSV2 - Web Client Linked View User Settings

- **Tabla:** WSV2
- **Descripción:** Web Client Linked View User Settings
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WSV2.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ParentId` | Parent ID | nVarChar | 40 | [OWSV](OWSV.md) |  |  |
| 2 | `UserId` | User ID | Int | 11 | - |  |  |
| 3 | `IsActive` | Is Active | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ParentId, UserId |
