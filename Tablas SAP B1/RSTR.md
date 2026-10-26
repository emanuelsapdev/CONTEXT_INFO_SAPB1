# RSTR - STRL resource

- **Tabla:** RSTR
- **Descripción:** STRL resource
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RSTR.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Created` | Creation date | Date | 8 | - |  |  |
| 2 | `Updated` | Update date | Date | 8 | - |  |  |
| 3 | `Language` | Language code | Int | 11 | - |  |  |
| 4 | `Name` | STRL name | nVarChar | 64 | - |  |  |
| 5 | `Num` | STRL number | Int | 11 | - |  |  |
| 6 | `MaxUnique` | Max Unique | Int | 11 | - |  |  |

## Claves e índices (4)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Language, Name |
| NUM | Yes | Language, Num |
| M_NUM | No | Num |
| M_NAME | No | Name |
