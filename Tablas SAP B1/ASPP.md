# ASPP - Special Prices

- **Tabla:** ASPP
- **Descripción:** Special Prices
- **Cantidad de campos:** 17
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ASPP.html

## Campos (17)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 2 | `CardCode` | BP Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 3 | `Price` | Special Price | Num | 19.6 | - |  |  |
| 4 | `Currency` | Price Currency | nVarChar | 3 | - |  |  |
| 5 | `Discount` | Discount in % | Num | 19.6 | - |  |  |
| 6 | `ListNum` | Price List No. | Int | 6 | [OPLN](OPLN.md) | 0 |  |
| 7 | `AutoUpdt` | Auto Update | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 8 | `EXPAND` | Item Details | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 9 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 10 | `SrcPrice` | Source Price | Int | 6 | - | 0 | `0` = Unit Price - Pri. Crcy<br>`1` = Unit Price - Add. Crcy 1<br>`2` = Unit Price - Add. Crcy 2 |
| 11 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 12 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 13 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 14 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 15 | `Valid` | Active | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 16 | `ValidFrom` | Active From | Date | 8 | - |  |  |
| 17 | `ValidTo` | Active To | Date | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CardCode, ItemCode, LogInstanc |
