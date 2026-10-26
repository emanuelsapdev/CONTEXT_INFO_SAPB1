# ARI1 - Add-On

- **Tabla:** ARI1
- **Descripción:** Add-On
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ARI1.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `USER_CODE` | User Code | nVarChar | 25 | [OUSR](OUSR.md) |  |  |
| 2 | `AddOnID` | Add-On ID | Int | 11 | - |  |  |
| 3 | `AddOnType` | Add-On Type | VarChar | 1 | - |  | `M` = Manual<br>`C` = Critical<br>`A` = Automatic<br>`D` = Disabled |
| 4 | `EnableFlag` | Add-On Enable Flag | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | USER_CODE, AddOnID |
