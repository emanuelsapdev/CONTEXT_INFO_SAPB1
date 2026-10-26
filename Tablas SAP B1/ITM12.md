# ITM12 - UoM in Item

- **Tabla:** ITM12
- **Descripción:** UoM in Item
- **Cantidad de campos:** 23
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ITM12.html

## Campos (23)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 2 | `UomType` | UoM Type | VarChar | 1 | - | P | `P` = Purchasing<br>`S` = Sales<br>`I` = Inventory |
| 3 | `UomEntry` | UoM Entry | Int | 11 | [OUOM](OUOM.md) |  |  |
| 4 | `BcdEntDft` | Default Bar Code Entry | Int | 11 | [OBCD](OBCD.md) |  |  |
| 5 | `PkgCodeDft` | Default Package Code | Int | 11 | [OPKG](OPKG.md) |  |  |
| 6 | `Height1` | Height 1 | Num | 19.6 | - |  |  |
| 7 | `Hght1Unit` | Height 1 UoM | Int | 6 | - |  |  |
| 8 | `Height2` | Height 2 | Num | 19.6 | - |  |  |
| 9 | `Hght2Unit` | Height 2 UoM | Int | 6 | - |  |  |
| 10 | `Width1` | Width 1 | Num | 19.6 | - |  |  |
| 11 | `Wdth1Unit` | Width 1 UoM | Int | 6 | - |  |  |
| 12 | `Width2` | Width 2 | Num | 19.6 | - |  |  |
| 13 | `Wdth2Unit` | Width 2 UoM | Int | 6 | - |  |  |
| 14 | `Length1` | Length 1 | Num | 19.6 | - |  |  |
| 15 | `Len1Unit` | Length 1 UoM | Int | 6 | - |  |  |
| 16 | `Length2` | Length 2 | Num | 19.6 | - |  |  |
| 17 | `Len2Unit` | Length 2 UoM | Int | 6 | - |  |  |
| 18 | `Volume` | Volume | Num | 19.6 | - |  |  |
| 19 | `VolUnit` | Volume UoM | Int | 6 | - |  |  |
| 20 | `Weight1` | Weight 1 | Num | 19.6 | - |  |  |
| 21 | `Wght1Unit` | Weight 1 UoM | Int | 6 | - |  |  |
| 22 | `Weight2` | Weight 2 | Num | 19.6 | - |  |  |
| 23 | `Wght2Unit` | Weight 2 UoM | Int | 6 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ItemCode, UomType, UomEntry |
| UOM_ENTRY | No | UomEntry |
