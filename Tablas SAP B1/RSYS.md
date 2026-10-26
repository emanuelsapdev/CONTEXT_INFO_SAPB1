# RSYS - System Strings

- **Tabla:** RSYS
- **Descripción:** System Strings
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RSYS.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Num` | String number | Int | 11 | - |  |  |
| 2 | `String` | String | nVarChar | 250 | - |  |  |
| 3 | `StringType` | String Type | Int | 6 | - | 0 | `0` = Free Text<br>`1` = Form<br>`2` = Table<br>`3` = Resource |
| 4 | `RefCounter` | Reference Counter | Int | 11 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Num |
| STRING | Yes | String |
