# SPP2 - Special Prices - Quantity Areas

- **Tabla:** SPP2
- **Descripción:** Special Prices - Quantity Areas
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SPP2.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ItemCode` | Item No. | nVarChar | 50 | [OSPP](OSPP.md) |  |  |
| 2 | `CardCode` | BP Code | nVarChar | 15 | [OSPP](OSPP.md) |  |  |
| 3 | `SPP1LNum` | Dates Row Number | Int | 6 | - |  |  |
| 4 | `SPP2LNum` | Row Number | Int | 6 | - |  |  |
| 5 | `Amount` | Quantity | Num | 19.6 | - |  |  |
| 6 | `Price` | Special Price | Num | 19.6 | - |  |  |
| 7 | `Currency` | Price Currency | nVarChar | 3 | - |  |  |
| 8 | `Discount` | Discount in % | Num | 19.6 | - |  |  |
| 9 | `UomEntry` | UoM Entry | Int | 11 | [OUOM](OUOM.md) |  |  |
| 10 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |

## Claves e índices (4)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CardCode, ItemCode, SPP1LNum, SPP2LNum |
| CARD | No | CardCode |
| ITEM | No | ItemCode |
| CURRENCY | No | Currency |
