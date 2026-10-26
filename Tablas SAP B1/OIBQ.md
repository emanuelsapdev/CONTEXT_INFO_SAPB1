# OIBQ - Item - Bin Accumulator

- **Tabla:** OIBQ
- **Descripción:** Item - Bin Accumulator
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OIBQ.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `ItemCode` | Item Code | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 3 | `BinAbs` | Bin Internal Number | Int | 11 | [OBIN](OBIN.md) |  |  |
| 4 | `OnHandQty` | On-Hand Quantity | Num | 19.6 | - |  |  |
| 5 | `WhsCode` | Warehouse Code | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 6 | `Freezed` | Item Frozen in Bin Location | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 7 | `FreezeDoc` | Inventory Count Doc. Frozen By | Int | 11 | [OINC](OINC.md) |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| BUSINESS_K | Yes | ItemCode, BinAbs |
| BIN_ABS | No | BinAbs |
