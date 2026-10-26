# RDN8 - Returns - Items in Package

- **Tabla:** RDN8
- **Descripción:** Returns - Items in Package
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RDN8.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | [ORDN](ORDN.md) |  |  |
| 2 | `PackageNum` | Package Number | Int | 11 | - |  |  |
| 3 | `ItemCode` | Item Code | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 4 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 5 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 6 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 16 |  |
| 7 | `UomEntry` | UoM Entry | Int | 11 | [OUOM](OUOM.md) | 0 |  |
| 8 | `unitMsr` | Unit | nVarChar | 100 | - |  |  |
| 9 | `NumPerMsr` | UoM Value | Num | 19.6 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, PackageNum, ItemCode, UomEntry, NumPerMsr |
