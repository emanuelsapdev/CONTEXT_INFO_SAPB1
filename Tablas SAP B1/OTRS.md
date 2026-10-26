# OTRS - Tax Report Saving Object

- **Tabla:** OTRS
- **Descripción:** Tax Report Saving Object
- **Cantidad de campos:** 16
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OTRS.html

## Campos (16)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `ObjType` | Object Type | nVarChar | 20 | - |  |  |
| 3 | `ReportType` | Report Type | Int | 11 | - |  | `1` = VAT Report (UK) |
| 4 | `PeriodType` | Report Period Type | VarChar | 1 | - |  | `Y` = Year<br>`Q` = Quarter<br>`B` = Bi-Monthly<br>`M` = Month<br>`P` = Period<br>`F` = Fiscal Year<br>`G` = Fiscal Quarter |
| 5 | `PeriodNum` | Report Period Number | Int | 11 | - |  |  |
| 6 | `Year` | Report Year | Int | 6 | - |  |  |
| 7 | `AdjustNum` | Report Adjustment Number | Int | 6 | - |  |  |
| 8 | `ApUserSign` | Approved By (User Signature) | Int | 6 | - |  |  |
| 9 | `ApDate` | Approval Date | Date | 8 | - |  |  |
| 10 | `ApTime` | Approval Time | Int | 6 | - |  |  |
| 11 | `DeclType` | Declaration Type | VarChar | 1 | - | O | `O` = Original<br>`S` = Substitute<br>`C` = Complementary |
| 12 | `SCDateFrom` | Selection Criteria - Date From | Date | 8 | - |  |  |
| 13 | `SCDateTo` | Selection Criteria - Date To | Date | 8 | - |  |  |
| 14 | `BosCode` | Box Set Code | Int | 11 | [OBOS](OBOS.md) |  |  |
| 15 | `BatchNum` | Journal Voucher No. | Int | 11 | [OBTD](OBTD.md) |  |  |
| 16 | `GstRtType` | GTS Return Type | nVarChar | 10 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
