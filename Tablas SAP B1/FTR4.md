# FTR4 - Transfer - Change Location

- **Tabla:** FTR4
- **Descripción:** Transfer - Change Location
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/FTR4.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | [OFTR](OFTR.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `ItemCode` | Item Code | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 4 | `CurLoc` | Current Location | Int | 11 | [OLCT](OLCT.md) |  |  |
| 5 | `NewLoc` | New Location | Int | 11 | [OLCT](OLCT.md) |  |  |
| 6 | `NBV` | Net Book Value | Num | 19.6 | - |  |  |
| 7 | `Quantity` | Quantity | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum |
