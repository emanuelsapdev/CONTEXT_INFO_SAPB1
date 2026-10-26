# VRT1 - Tax Invoice Report - Rows

- **Tabla:** VRT1
- **Descripción:** Tax Invoice Report - Rows
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/VRT1.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TxInvRptNo` | Tax Invoice Report No. | nVarChar | 10 | [OVRT](OVRT.md) |  |  |
| 2 | `SeqNo` | Sequence No. | Int | 11 | - |  |  |
| 3 | `MD` | Original Date of Line Item | Date | 8 | - |  |  |
| 4 | `ItemDesc` | Description of Line Item | nVarChar | 200 | - |  |  |
| 5 | `Unit` | Unit of Line Item | nVarChar | 100 | - |  |  |
| 6 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 7 | `UnitPrice` | Unit Price | Num | 19.6 | - |  |  |
| 8 | `BaseAmt` | Base Amount | Num | 19.6 | - |  |  |
| 9 | `TaxAmt` | Tax Amount | Num | 19.6 | - |  |  |
| 10 | `Remark` | Remarks | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TxInvRptNo, SeqNo |
