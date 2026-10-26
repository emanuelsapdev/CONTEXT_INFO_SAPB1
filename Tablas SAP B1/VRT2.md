# VRT2 - Tax Invoice Report Grid Info

- **Tabla:** VRT2
- **Descripción:** Tax Invoice Report Grid Info
- **Cantidad de campos:** 21
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/VRT2.html

## Campos (21)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TxInvRptNo` | Tax Invoice Report No. | nVarChar | 10 | [OVRT](OVRT.md) |  |  |
| 2 | `GridRow` | Grid Row Number | Int | 11 | - |  |  |
| 3 | `BPLId` | Business Place ID | Int | 11 | - |  |  |
| 4 | `BPCode` | BP Code | nVarChar | 15 | - |  |  |
| 5 | `BPName` | BP Name | nVarChar | 200 | - |  |  |
| 6 | `DocDate` | Doc. Date | Date | 8 | - |  |  |
| 7 | `ItemNo` | Item Number | nVarChar | 50 | - |  |  |
| 8 | `ItemDes` | Item Description | nVarChar | 200 | - |  |  |
| 9 | `TaxCode` | Tax Code | nVarChar | 8 | - |  |  |
| 10 | `ItemQty` | Item Quantity | Num | 19.6 | - |  |  |
| 11 | `ItemPrice` | Item Price | Num | 19.6 | - |  |  |
| 12 | `BaseAmt` | Base Amount | Num | 19.6 | - |  |  |
| 13 | `TaxAmt` | Tax Amount | Num | 19.6 | - |  |  |
| 14 | `LineType` | Row Type | Int | 11 | - |  |  |
| 15 | `DocEntry` | Unique Document ID | Int | 11 | - |  |  |
| 16 | `DocType` | Document Type | Int | 11 | - |  | `0`<br>`13` = A/R Invoice<br>`14` = A/R Credit Memo<br>`203` = A/R Down Payment |
| 17 | `LineNum` | Item Row Number | Int | 11 | - |  |  |
| 18 | `Currency` | Currency | nVarChar | 3 | - |  |  |
| 19 | `Remark` | Remarks | nVarChar | 100 | - |  |  |
| 20 | `LegacyData` | Legacy Data | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 21 | `Quantity` | Quantity | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TxInvRptNo, GridRow |
