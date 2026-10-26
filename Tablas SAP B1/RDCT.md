# RDCT - Dictionary

- **Tabla:** RDCT
- **Descripción:** Dictionary
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RDCT.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Language` | Language code | Int | 11 | - |  |  |
| 2 | `Num` | String number | Int | 11 | - |  |  |
| 3 | `String` | String | nVarChar | 250 | - |  |  |
| 4 | `Updated` | Update date | Date | 8 | - |  |  |
| 5 | `UpdateTime` | Update Time | Int | 6 | - | 0 |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Language, Num |
| STRING | No | Language, String |
| NUM | No | Num |
