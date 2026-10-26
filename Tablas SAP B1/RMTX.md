# RMTX - MATX resource

- **Tabla:** RMTX
- **Descripción:** MATX resource
- **Cantidad de campos:** 16
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RMTX.html

## Campos (16)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Created` | Creation date | Date | 8 | - |  |  |
| 2 | `Updated` | Update date | Date | 8 | - |  |  |
| 3 | `Language` | Language code | Int | 11 | - |  |  |
| 4 | `Name` | MATX name | nVarChar | 64 | - |  |  |
| 5 | `Num` | MATX number | Int | 11 | - |  |  |
| 6 | `DoColor` | Use color table | VarChar | 1 | - | 0 | `0` = No<br>`1` = Yes |
| 7 | `BorderRed` | Border red | Int | 11 | - |  |  |
| 8 | `BorderGrn` | Border green | Int | 11 | - |  |  |
| 9 | `BorderBlue` | Border blue | Int | 11 | - |  |  |
| 10 | `BgRed` | Background red | Int | 11 | - |  |  |
| 11 | `BgGreen` | Background green | Int | 6 | - |  |  |
| 12 | `BgBlue` | Background blue | Int | 11 | - |  |  |
| 13 | `CellHeight` | Cell height | Int | 11 | - |  |  |
| 14 | `TitleHeigt` | Title height | Int | 11 | - |  |  |
| 15 | `Width` | Width | Int | 11 | - |  |  |
| 16 | `MaxUnique` | Max Unique | Int | 11 | - |  |  |

## Claves e índices (4)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Language, Name |
| NUM | Yes | Language, Num |
| M_NAME | No | Name |
| M_NUM | No | Num |
