# OWNOT - Notifications

- **Tabla:** OWNOT
- **Descripción:** Notifications
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OWNOT.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Guid` | Guid | nVarChar | 40 | - |  |  |
| 2 | `UserId` | User Id | Int | 11 | - |  |  |
| 3 | `Date` | Activity Date | Date | 8 | - |  |  |
| 4 | `Read` | Read/Unread status | VarChar | 1 | - |  |  |
| 5 | `Dismissed` | Dismissed or not | VarChar | 1 | - |  |  |
| 6 | `NotiType` | Notification Type | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Guid |
