# REQ1 - External System Call Request - Message List

- **Tabla:** REQ1
- **Descripción:** External System Call Request - Message List
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/REQ1.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Request ID | Int | 11 | [OREQ](OREQ.md) |  |  |
| 2 | `LineId` | Message Line ID | Int | 11 | - |  |  |
| 3 | `MsgType` | Message Type | VarChar | 1 | - | I | `I` = Information<br>`W` = Warning<br>`E` = Error |
| 4 | `ErrCode` | Error Code | nVarChar | 3 | - |  |  |
| 5 | `MsgBody` | Message Body | Text | 16 | - |  |  |
| 6 | `Status` | Message Status | VarChar | 1 | - | U | `U` = Unread<br>`R` = Read |
| 7 | `MsgDate` | Message Log Date | Date | 8 | - |  |  |
| 8 | `MsgTime` | Message Log Time | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineId |
