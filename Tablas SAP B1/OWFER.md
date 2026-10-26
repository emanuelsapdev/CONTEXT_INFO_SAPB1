# OWFER - Workflow Error Message

- **Tabla:** OWFER
- **Descripción:** Workflow Error Message
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OWFER.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Identity | 11 | - |  |  |
| 2 | `MsgID` | Message ID | nVarChar | 64 | - |  |  |
| 3 | `MsgDetails` | Message Details | Text | 16 | - |  |  |
| 4 | `CreateDate` | Create Date - History | Date | 8 | - |  |  |
| 5 | `UserSign` | Updating User - History | Int | 6 | [OUSR](OUSR.md) |  |  |
| 6 | `CreateTime` | Create Time | Int | 11 | - |  |  |
| 7 | `MsgTaskID` | Message Task ID | nVarChar | 6 | - |  |  |
| 8 | `MsgErrSrc` | Message Source | nVarChar | 20 | - |  |  |
| 9 | `Remark` | Remarks | Text | 16 | - |  |  |
| 10 | `MsgType` | Message Type | VarChar | 1 | - |  | `I` = Information<br>`E` = Error<br>`W` = Warning |
| 11 | `MsgInstID` | Message Instance ID | Int | 11 | - |  |  |
| 12 | `TemplateID` | Template ID | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
