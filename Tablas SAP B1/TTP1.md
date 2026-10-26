# TTP1 - ToolTip Preview - Rows

- **Tabla:** TTP1
- **Descripción:** ToolTip Preview - Rows
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TTP1.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 2 | `ObjectId` | Object ID | Int | 11 | - |  |  |
| 3 | `DataKey` | Data Key | nVarChar | 50 | - |  |  |
| 4 | `VisOrder` | Visual Order | Int | 11 | - |  |  |
| 5 | `IsVisible` | Visible | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | UserSign, ObjectId, DataKey |
