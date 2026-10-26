# OASG - Account Segmentation

- **Tabla:** OASG
- **Descripción:** Account Segmentation
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OASG.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Numerator | Int | 6 | - |  |  |
| 2 | `Name` | Name | nVarChar | 100 | - |  |  |
| 3 | `Size` | Size | Int | 6 | - |  |  |
| 4 | `Type` | Type | VarChar | 1 | - | A | `A` = Alphanumeric<br>`N` = Numeric |
| 5 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId |
