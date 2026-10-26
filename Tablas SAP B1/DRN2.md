# DRN2 - Depreciation Run - Posting - Asset

- **Tabla:** DRN2
- **Descripción:** Depreciation Run - Posting - Asset
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/DRN2.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | [ODRN](ODRN.md) |  |  |
| 2 | `AcctDtn` | Account Determination | nVarChar | 15 | [OADT](OADT.md) |  |  |
| 3 | `ItemCode` | Item Code | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 4 | `OrdDprAmt` | Ordinary Depreciation Amount | Num | 19.6 | - |  |  |
| 5 | `SpDprAmt` | Special Depreciation Amount | Num | 19.6 | - |  |  |
| 6 | `RevReserve` | Revaluation Reserve Amount | Num | 19.6 | - |  |  |
| 7 | `AssetClass` | Asset Class | nVarChar | 20 | [OACS](OACS.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, AssetClass, ItemCode |
