# OZRD - POS Daily Summary

- **Tabla:** OZRD
- **Descripción:** POS Daily Summary
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OZRD.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `DocDate` | Document Date | Date | 8 | - |  |  |
| 3 | `POSEquipNo` | POS Equipment No. | nVarChar | 20 | [OPOS](OPOS.md) |  |  |
| 4 | `ResetCntr` | Reset Counter | Int | 11 | - |  |  |
| 5 | `SummaryCnt` | Summary Counter | Int | 11 | - |  |  |
| 6 | `OperCntr` | Operation Counter | Int | 11 | - |  |  |
| 7 | `TotalSum` | Total Sum | Num | 19.6 | - |  |  |
| 8 | `GrossSale` | Gross Sale Sum | Num | 19.6 | - |  |  |
| 9 | `PISSum` | PIS Sum | Num | 19.6 | - |  |  |
| 10 | `COFINSSum` | COFINS Sum | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
