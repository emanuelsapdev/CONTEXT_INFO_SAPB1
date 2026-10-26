# TABL - Table resource

- **Tabla:** TABL
- **Descripción:** Table resource
- **Cantidad de campos:** 18
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TABL.html

## Campos (18)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Created` | Creation date | Date | 8 | - |  |  |
| 2 | `Updated` | Update date | Date | 8 | - |  |  |
| 3 | `Name` | Table name | nVarChar | 64 | - |  |  |
| 4 | `Num` | Table number | Int | 11 | - |  |  |
| 5 | `DoColor` | Use color table | VarChar | 1 | - | 0 | `0` = No<br>`1` = Yes |
| 6 | `BorderRed` | Border red | Int | 11 | - |  |  |
| 7 | `BorderGrn` | Border green | Int | 11 | - |  |  |
| 8 | `BorderBlue` | Border blue | Int | 11 | - |  |  |
| 9 | `BgRed` | Background red | Int | 11 | - | 65535 |  |
| 10 | `BgGreen` | Background green | Int | 11 | - | 65535 |  |
| 11 | `BgBlue` | Background blue | Int | 11 | - | 65535 |  |
| 12 | `CellHeight` | Cell height | Int | 11 | - |  |  |
| 13 | `TitleHeigt` | Title height | Int | 11 | - |  |  |
| 14 | `Width` | Width | Int | 11 | - |  |  |
| 15 | `MaxUnique` | Max Unique | Int | 11 | - |  |  |
| 16 | `UsrSgnAttr` | User Sign For Attribs Change | Int | 11 | - | -1 |  |
| 17 | `ResCode` | Resource Code from RSBD | Int | 11 | - | -1 |  |
| 18 | `RevCode` | Revision Code | Int | 11 | - | -1 |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Name, ResCode, RevCode |
| NUM | Yes | Num |
