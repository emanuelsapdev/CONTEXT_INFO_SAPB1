# OPKG - Package Types

- **Tabla:** OPKG
- **Descripción:** Package Types
- **Cantidad de campos:** 20
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OPKG.html

## Campos (20)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `PkgCode` | Code | Int | 11 | - |  |  |
| 2 | `PkgType` | Type | nVarChar | 30 | - |  |  |
| 3 | `Length1` | Length 1 | Num | 19.6 | - |  |  |
| 4 | `Len1Unit` | Unit of Length 1 | Int | 6 | - |  |  |
| 5 | `length2` | Length 2 | Num | 19.6 | - |  |  |
| 6 | `Len2Unit` | Unit of Length 2 | Int | 6 | - |  |  |
| 7 | `Width1` | Width 1 | Num | 19.6 | - |  |  |
| 8 | `Wdth1Unit` | Unit of Width 1 | Int | 6 | - |  |  |
| 9 | `Width2` | Width 2 | Num | 19.6 | - |  |  |
| 10 | `Wdth2Unit` | Unit of Width 2 | Int | 6 | - |  |  |
| 11 | `Height1` | Height 1 | Num | 19.6 | - |  |  |
| 12 | `Hght1Unit` | Unit of Height 1 | Int | 6 | - |  |  |
| 13 | `Height2` | Height 2 | Num | 19.6 | - |  |  |
| 14 | `Hght2Unit` | Unit of Height 2 | Int | 6 | - |  |  |
| 15 | `Volume` | Volume | Num | 19.6 | - |  |  |
| 16 | `VolUnit` | Volume UoM | Int | 6 | - |  |  |
| 17 | `Weight1` | Weight 1 | Num | 19.6 | - |  |  |
| 18 | `WghtUnit` | Weight UoM | Int | 6 | - |  |  |
| 19 | `Weight2` | Weight 2 | Num | 19.6 | - |  |  |
| 20 | `Wght2Unit` | Unit of Weight 2 | Int | 6 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | PkgCode |
| TYPE | Yes | PkgType |
