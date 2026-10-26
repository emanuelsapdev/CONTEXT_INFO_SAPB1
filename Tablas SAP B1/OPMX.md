# OPMX - Payroll

- **Tabla:** OPMX
- **Descripción:** Payroll
- **Cantidad de campos:** 13
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OPMX.html

## Campos (13)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `Total` | Total | Num | 19.6 | - |  |  |
| 3 | `Currency` | Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 4 | `Rate` | Exchange Rate | Num | 19.6 | - |  |  |
| 5 | `Uid` | UUID of payroll | nVarChar | 100 | - |  |  |
| 6 | `RFC` | RFC | nVarChar | 20 | - |  |  |
| 7 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 8 | `FileDate` | File Date | Date | 8 | - |  |  |
| 9 | `FileName` | Imported File Name | nVarChar | 254 | - |  |  |
| 10 | `JVBatchNum` | Journal Voucher Batch Number | Int | 11 | [OBTF](OBTF.md) |  |  |
| 11 | `JVTransId` | Journal Voucher Trans Number | Int | 11 | [OBTF](OBTF.md) |  |  |
| 12 | `JETransId` | Journal Entry Trans Number | Int | 11 | [OJDT](OJDT.md) |  |  |
| 13 | `Type` | Type | VarChar | 1 | - | P | `P` = Payroll<br>`E` = Expenses |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| UID | Yes | Uid |
