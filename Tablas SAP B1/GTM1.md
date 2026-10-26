# GTM1 - GTS Mapping Object Details

- **Tabla:** GTM1
- **Descripción:** GTS Mapping Object Details
- **Cantidad de campos:** 17
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/GTM1.html

## Campos (17)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [OGTM](OGTM.md) |  |  |
| 2 | `LineNum` | Line Number | Int | 11 | - |  |  |
| 3 | `ItemCode` | Item Code | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 4 | `ItemName` | Item Name | nVarChar | 200 | - |  |  |
| 5 | `ItemUoM` | Item UoM | nVarChar | 100 | - |  |  |
| 6 | `ItemSpec` | Item Spec. | nVarChar | 30 | - |  |  |
| 7 | `ItemTaxCat` | Item Tax Category | nVarChar | 4 | - |  |  |
| 8 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 9 | `Amount` | Amount | Num | 19.6 | - |  |  |
| 10 | `VatPercent` | VAT Percent | Num | 19.6 | - |  |  |
| 11 | `DiscRate` | Discount Rate | Num | 19.6 | - |  |  |
| 12 | `DiscAmount` | Discount Amount | Num | 19.6 | - |  |  |
| 13 | `VatAmount` | VAT Amount | Num | 19.6 | - |  |  |
| 14 | `DiscVatAmt` | Discount VAT Amount | Num | 19.6 | - |  |  |
| 15 | `UnitPrice` | Unit Price | Num | 19.6 | - |  |  |
| 16 | `UPirceType` | Unit Price Type | VarChar | 1 | - | 0 | `0` = Net<br>`1` = Gross |
| 17 | `TaxCatCode` | Item Tax Category Code | nVarChar | 50 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineNum |
