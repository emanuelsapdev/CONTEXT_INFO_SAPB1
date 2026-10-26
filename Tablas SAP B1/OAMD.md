# OAMD - Amount Differences Report

- **Tabla:** OAMD
- **Descripción:** Amount Differences Report
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OAMD.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `LineNum` | Internal ID | Int | 11 | - |  |  |
| 2 | `DateFrom` | Date From | Date | 8 | - |  |  |
| 3 | `DateTo` | Date To | Date | 8 | - |  |  |
| 4 | `CardCode` | BP Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 5 | `Approved` | Confirmed | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `AmountDiff` | Amount Difference (LC) | Num | 19.6 | - |  |  |
| 7 | `TaxAmtDiff` | Tax Difference (LC) | Num | 19.6 | - |  |  |
| 8 | `RpCurrency` | Currency Chosen for the Report | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 9 | `VendOffAct` | Vendor Offset Account | nVarChar | 15 | [OACT](OACT.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | LineNum |
