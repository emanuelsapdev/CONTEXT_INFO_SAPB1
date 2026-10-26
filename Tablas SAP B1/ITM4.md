# ITM4 - Package in Items

- **Tabla:** ITM4
- **Descripción:** Package in Items
- **Cantidad de campos:** 23
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ITM4.html

## Campos (23)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 2 | `UomType` | UoM Type | VarChar | 1 | - | P | `P` = Purchasing<br>`S` = Sales |
| 3 | `UomEntry` | UoM Entry | Int | 11 | [OUOM](OUOM.md) |  |  |
| 4 | `PkgCode` | Package Code | Int | 11 | [OPKG](OPKG.md) |  |  |
| 5 | `Height1` | Height 1 | Num | 19.6 | - |  |  |
| 6 | `Hght1Unit` | Height 1 UoM | Int | 6 | - |  |  |
| 7 | `Height2` | Height 2 | Num | 19.6 | - |  |  |
| 8 | `Hght2Unit` | Height 2 UoM | Int | 6 | - |  |  |
| 9 | `Width1` | Width 1 | Num | 19.6 | - |  |  |
| 10 | `Wdth1Unit` | Width 1 UoM | Int | 6 | - |  |  |
| 11 | `Width2` | Width 2 | Num | 19.6 | - |  |  |
| 12 | `Wdth2Unit` | Width 2 UoM | Int | 6 | - |  |  |
| 13 | `Length1` | Length 1 | Num | 19.6 | - |  |  |
| 14 | `Len1Unit` | Length 1 UoM | Int | 6 | - |  |  |
| 15 | `Length2` | Length 2 | Num | 19.6 | - |  |  |
| 16 | `Len2Unit` | Length 2 UoM | Int | 6 | - |  |  |
| 17 | `Volume` | Volume | Num | 19.6 | - |  |  |
| 18 | `VolUnit` | Volume UoM | Int | 6 | - |  |  |
| 19 | `Weight1` | Weight 1 | Num | 19.6 | - |  |  |
| 20 | `Wght1Unit` | Weight 1 UoM | Int | 6 | - |  |  |
| 21 | `Weight2` | Weight 2 | Num | 19.6 | - |  |  |
| 22 | `Wght2Unit` | Weight 2 UoM | Int | 6 | - |  |  |
| 23 | `QtyPerPack` | Quantity per Packaging UoM | Num | 19.6 | - |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ItemCode, UomType, UomEntry, PkgCode |
| PKG_CODE | No | PkgCode |
| UOM_ENTRY | No | UomEntry |
