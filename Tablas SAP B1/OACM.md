# OACM - Accumulation

- **Tabla:** OACM
- **Descripción:** Accumulation
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OACM.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Internal Number | Int | 11 | - |  |  |
| 2 | `CardCode` | Customer/Vendor Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 3 | `WTCode` | WTax Code | nVarChar | 4 | [OWHT](OWHT.md) |  |  |
| 4 | `PeriodCat` | Period Category | nVarChar | 20 | - |  |  |
| 5 | `AcmAmt` | Accumulation Amount | Num | 19.6 | - |  |  |
| 6 | `ExcdTransc` | Exceed Transaction Threshold | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 7 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 8 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId |
| ACCUM | No | CardCode, WTCode, PeriodCat |
