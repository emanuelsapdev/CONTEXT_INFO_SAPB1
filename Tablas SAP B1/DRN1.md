# DRN1 - Depreciation Run - Posting

- **Tabla:** DRN1
- **Descripción:** Depreciation Run - Posting
- **Cantidad de campos:** 14
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/DRN1.html

## Campos (14)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | [ODRN](ODRN.md) |  |  |
| 2 | `AcctDtn` | Account Determination | nVarChar | 15 | [OADT](OADT.md) |  |  |
| 3 | `TransId` | Transaction Number | Int | 11 | [OJDT](OJDT.md) |  |  |
| 4 | `OrdDprAct` | Ordinary Depreciation Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 5 | `SpDprAct` | Special Depreciation Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 6 | `SpBalAct` | Special Balance Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 7 | `OrdBalAct` | Ordinary Balance Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 8 | `OrdDprAmt` | Ordinary Depreciation Amount | Num | 19.6 | - |  |  |
| 9 | `SpDprAmt` | Special Depreciation Amount | Num | 19.6 | - |  |  |
| 10 | `RevResAct` | Revaluation Reserve Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 11 | `RevResClr` | Revaluation Reserve Clearing | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 12 | `RevReserve` | Revaluation Reserve Amount | Num | 19.6 | - |  |  |
| 13 | `AssetClass` | Asset Class | nVarChar | 20 | [OACS](OACS.md) |  |  |
| 14 | `CancelId` | Cancelation Transaction No. | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, AssetClass |
