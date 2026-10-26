# STRL - String List resource

- **Tabla:** STRL
- **Descripción:** String List resource
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/STRL.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Created` | Creation date | Date | 8 | - |  |  |
| 2 | `Updated` | Update date | Date | 8 | - |  |  |
| 3 | `Name` | STRL name | nVarChar | 64 | - |  |  |
| 4 | `Num` | STRL number | Int | 11 | - |  |  |
| 5 | `MaxUnique` | Max Unique | Int | 11 | - |  |  |
| 6 | `RobjCode` | Imp Exp Obj Code | Int | 11 | - | 0 |  |
| 7 | `UsrSgnAttr` | User Sign For Attribs Change | Int | 11 | - | -1 |  |
| 8 | `ResCode` | Resource Code from RSBD | Int | 11 | - | -1 |  |
| 9 | `RevCode` | Revision Code | Int | 11 | - | -1 |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Name, ResCode, RevCode |
| NUM | Yes | Num |
