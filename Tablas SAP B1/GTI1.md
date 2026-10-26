# GTI1 - GTS Invoice Details

- **Tabla:** GTI1
- **Descripción:** GTS Invoice Details
- **Cantidad de campos:** 13
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/GTI1.html

## Campos (13)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [OGTI](OGTI.md) |  |  |
| 2 | `LineNum` | Line Number | Int | 11 | - |  |  |
| 3 | `DisctLine` | Discount Flag | VarChar | 1 | - | 0 | `0` = Normal<br>`1` = Discount Line |
| 4 | `ItemName` | Item Name | nVarChar | 60 | - |  |  |
| 5 | `ItemSpec` | Item Specification | nVarChar | 30 | - |  |  |
| 6 | `Uom` | Unit of Measurement | nVarChar | 16 | - |  |  |
| 7 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 8 | `NetAmount` | Net Amount | Num | 19.6 | - |  |  |
| 9 | `VatPercent` | VAT Percent | Num | 19.6 | - |  |  |
| 10 | `VatAmount` | VAT Amount | Num | 19.6 | - |  |  |
| 11 | `UnitPrice` | Unit Price | Num | 19.6 | - |  |  |
| 12 | `UnitPricTp` | Unit Price Type | VarChar | 1 | - | 0 | `0` = Net<br>`1` = Gross |
| 13 | `ItemTaxCat` | Item Tax Category | nVarChar | 30 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineNum |
