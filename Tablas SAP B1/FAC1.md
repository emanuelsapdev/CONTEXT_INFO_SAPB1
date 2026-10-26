# FAC1 - Fixed Asset Parameter Change - Rows

- **Tabla:** FAC1
- **Descripción:** Fixed Asset Parameter Change - Rows
- **Cantidad de campos:** 14
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/FAC1.html

## Campos (14)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [OFAC](OFAC.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `DprArea` | Depreciation Area | nVarChar | 15 | [ODPA](ODPA.md) |  |  |
| 4 | `TransType` | Transaction Type | nVarChar | 4 | - |  | `0` = Unknown<br>`510` = Change of Depreciation Type<br>`520` = Change of Useful Life<br>`530` = Change of Depreciation Start Date<br>`540` = Change of Salvage Value<br>`560` = Change of Period Control |
| 5 | `OldDprType` | Old Depreciation Type | nVarChar | 15 | [ODTP](ODTP.md) |  |  |
| 6 | `NewDprType` | New Depreciation Type | nVarChar | 15 | [ODTP](ODTP.md) |  |  |
| 7 | `OldUsfLife` | Old Useful Life | Int | 11 | - |  |  |
| 8 | `NewUsfLife` | New Useful Life | Int | 11 | - |  |  |
| 9 | `OldDprDate` | Old Depreciation Start Date | Date | 8 | - |  |  |
| 10 | `NewDprDate` | New Depreciation Start Date | Date | 8 | - |  |  |
| 11 | `OldSalVal` | Old Salvage Value | Num | 19.6 | - |  |  |
| 12 | `NewSalVal` | New Salvage Value | Num | 19.6 | - |  |  |
| 13 | `OldTtlUnit` | Old Total Units | Int | 11 | - |  |  |
| 14 | `NewTtlUnit` | New Total Units | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineNum |
