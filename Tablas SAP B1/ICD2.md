# ICD2 - Inventory Counting Draft - UoM

- **Tabla:** ICD2
- **Descripción:** Inventory Counting Draft - UoM
- **Cantidad de campos:** 19
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ICD2.html

## Campos (19)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Number | Int | 11 | [OICD](OICD.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `ChildNum` | Child Number | Int | 11 | - |  |  |
| 4 | `BarCode` | Bar Code | nVarChar | 254 | - |  |  |
| 5 | `UomCode` | UoM Code | nVarChar | 20 | [OUOM](OUOM.md) |  |  |
| 6 | `UomQty` | UoM Counted Qty | Num | 19.6 | - |  |  |
| 7 | `CountQty` | Counted Qty of Inventory UoM | Num | 19.6 | - |  |  |
| 8 | `Tk1UomQty` | Counter 1 UoM Counted Qty | Num | 19.6 | - |  |  |
| 9 | `Tk2UomQty` | - | Num | 19.6 | - |  |  |
| 10 | `Tk1CntQty` | Counter 1 Counted Qty of Inv. | Num | 19.6 | - |  |  |
| 11 | `Tk2CntQty` | - | Num | 19.6 | - |  |  |
| 12 | `ItmsPerUnt` | Items per Unit | Num | 19.6 | - |  |  |
| 13 | `LogIns` | Log Instance - History | Int | 11 | - |  |  |
| 14 | `UgpEntry` | UoM Group Abs. Entry | Int | 11 | [OUGP](OUGP.md) |  |  |
| 15 | `TeamUomQty` | Team UoM Counted Qty | Num | 19.6 | - |  |  |
| 16 | `TeamCntQty` | Team Counted Qty | Num | 19.6 | - |  |  |
| 17 | `IUomEntry` | Inventory UoM Entry | nVarChar | 20 | [OUOM](OUOM.md) |  |  |
| 18 | `UomNum` | Uom Item Per Unit Numerator | Num | 19.6 | - |  |  |
| 19 | `UomDen` | Uom Item Per Unit Denominator | Num | 19.6 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum, ChildNum |
| BUSINESS | Yes | DocEntry, LineNum, BarCode, UomCode |
