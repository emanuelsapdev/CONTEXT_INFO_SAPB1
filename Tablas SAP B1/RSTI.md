# RSTI - STRI resource

- **Tabla:** RSTI
- **Descripción:** STRI resource
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RSTI.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Created` | Creation date | Date | 8 | - |  |  |
| 2 | `Updated` | Update date | Date | 8 | - |  |  |
| 3 | `Language` | Language code | Int | 11 | - |  |  |
| 4 | `Name` | STRL name | nVarChar | 64 | [STRL](STRL.md) |  |  |
| 5 | `Num` | String number | Int | 11 | - |  |  |
| 6 | `String` | String | nVarChar | 250 | - |  |  |
| 7 | `StringLen` | String length | Int | 11 | - |  |  |
| 8 | `UniqueID` | Unique ID | nVarChar | 10 | - |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Language, Name, Num |
| M_NUM | No | Name, Num |
| UNIQUE_ID | Yes | Language, Name, UniqueID |
