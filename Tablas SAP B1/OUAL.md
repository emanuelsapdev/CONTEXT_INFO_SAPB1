# OUAL - User Action Log

- **Tabla:** OUAL
- **Descripción:** User Action Log
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OUAL.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Id` | ID | Identity | 11 | - |  |  |
| 2 | `UserId` | User Id | Int | 6 | [OUSR](OUSR.md) |  |  |
| 3 | `ActionDate` | Action Date | Date | 8 | - |  |  |
| 4 | `ActionTime` | Action Time | Int | 11 | - |  |  |
| 5 | `ActionType` | Action Type | VarChar | 1 | - |  |  |
| 6 | `ObjectId` | Object Id | Int | 11 | - |  |  |
| 7 | `ObjectKey` | Object Key | nVarChar | 64 | - |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Id |
| TIME | No | ActionDate, ActionTime |
| ID_KEY | No | ObjectId, ObjectKey |
