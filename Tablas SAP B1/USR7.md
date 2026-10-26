# USR7 - Group User Association

- **Tabla:** USR7
- **Descripción:** Group User Association
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/USR7.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `UserId` | User ID | Int | 6 | [OUSR](OUSR.md) |  |  |
| 2 | `GroupId` | Group ID | Int | 6 | [OUGR](OUGR.md) |  |  |
| 3 | `Category` | Group Category | nVarChar | 155 | - |  |  |
| 4 | `StartDate` | Start Date | Date | 8 | - |  |  |
| 5 | `DueDate` | Due Date | Date | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | UserId, GroupId |
