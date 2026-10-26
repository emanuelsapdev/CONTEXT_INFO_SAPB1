# RTPL - Translation Problems Log

- **Tabla:** RTPL
- **Descripción:** Translation Problems Log
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RTPL.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Language` | Language Code | Int | 11 | - |  |  |
| 2 | `ResKey` | Resource Key | nVarChar | 15 | - |  |  |
| 3 | `Created` | Creation Date | Date | 8 | - |  |  |
| 4 | `CreateTime` | Generation Time | Int | 6 | - |  |  |
| 5 | `Updated` | Update Date | Date | 8 | - |  |  |
| 6 | `UpdateTime` | Update Time | Int | 6 | - |  |  |
| 7 | `UserText` | Memo | Text | 16 | - |  |  |
| 8 | `Attachment` | Attached File | Text | 16 | - |  |  |
| 9 | `UserName` | User Name | nVarChar | 254 | - |  |  |
| 10 | `E_Mail` | E-Mail | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Language, ResKey |
