# ENT1 - Entry - Rows

- **Tabla:** ENT1
- **Descripción:** Entry - Rows
- **Cantidad de campos:** 13
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ENT1.html

## Campos (13)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Entry | Int | 11 | [OINV](OINV.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `BaseEntry` | Base Document Internal ID | Int | 11 | - |  |  |
| 4 | `PackQty` | Packing Quantity | Num | 19.6 | - |  |  |
| 5 | `PurPackMsr` | Packaging UoM Name | nVarChar | 8 | - | Pack |  |
| 6 | `ArsnalName` | Storage Group Name | nVarChar | 20 | - |  |  |
| 7 | `ArsnalCode` | Storage Group Code | nVarChar | 20 | - |  |  |
| 8 | `UnitMsr` | Ref. UoM (Type) | nVarChar | 20 | - | Unit |  |
| 9 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 10 | `Fraction` | Remainder | Num | 19.6 | - |  |  |
| 11 | `Weight1` | Weight | Num | 19.6 | - |  |  |
| 12 | `LineTotal` | Row Total | Num | 19.6 | - |  |  |
| 13 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum |
