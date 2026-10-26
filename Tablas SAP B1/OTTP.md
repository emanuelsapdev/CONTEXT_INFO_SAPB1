# OTTP - ToolTip Preview

- **Tabla:** OTTP
- **Descripción:** ToolTip Preview
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OTTP.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 2 | `ObjectId` | Object ID | Int | 11 | - |  |  |
| 3 | `IsEnabled` | Enabled | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | UserSign, ObjectId |
