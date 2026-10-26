# TNN1 - 1099 Boxes

- **Tabla:** TNN1
- **Descripción:** 1099 Boxes
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TNN1.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `FormCode` | Form Code | Int | 11 | [OTNN](OTNN.md) |  |  |
| 2 | `Box1099` | 1099 Box | nVarChar | 20 | - |  |  |
| 3 | `BoxDescr` | Box Description | nVarChar | 100 | - |  |  |
| 4 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 5 | `Locked` | Locked | VarChar | 1 | - | N | `N` = Changeable<br>`Y` = Locked |
| 6 | `Min1099Amt` | Minimum 1099 Amount | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | FormCode, Box1099 |
