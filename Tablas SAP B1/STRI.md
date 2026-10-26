# STRI - String list item resource

- **Tabla:** STRI
- **Descripción:** String list item resource
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/STRI.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Created` | Creation date | Date | 8 | - |  |  |
| 2 | `Updated` | Update date | Date | 8 | - |  |  |
| 3 | `Name` | STRL name | nVarChar | 64 | - |  |  |
| 4 | `Num` | String number | Int | 11 | - |  |  |
| 5 | `StrIndex` | String Index | Int | 11 | - | 0 |  |
| 6 | `ItemString` | Item string | nVarChar | 254 | - |  |  |
| 7 | `UniqueID` | Unique ID | nVarChar | 10 | - |  |  |
| 8 | `UsrSgnStr` | User Sign For Strings Change | Int | 11 | - | -1 |  |
| 9 | `UsrSgnAttr` | User Sign For Attribs Change | Int | 11 | - | -1 |  |
| 10 | `ResCode` | Resource Code from RSBD | Int | 11 | - | -1 |  |
| 11 | `RevCode` | Revision Code | Int | 11 | - | -1 |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Name, Num, ResCode, RevCode |
| UNIQUE_ID | Yes | Name, UniqueID |
