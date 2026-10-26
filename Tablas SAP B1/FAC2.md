# FAC2 - Fixed Asset Parameter Change - Period Control Change

- **Tabla:** FAC2
- **Descripción:** Fixed Asset Parameter Change - Period Control Change
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/FAC2.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [OFAC](OFAC.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `DprArea` | Depreciation Area | nVarChar | 15 | [ODPA](ODPA.md) |  |  |
| 4 | `PeriodCat` | Period Category | nVarChar | 10 | - |  |  |
| 5 | `VisOrder` | Visual Order | Int | 11 | - |  |  |
| 6 | `OldDprSt` | Old Depreciation Status | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 7 | `NewDprSt` | New Depreciation Status | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 8 | `OldFactor` | Old Factor | Num | 19.6 | - |  |  |
| 9 | `NewFactor` | New Factor | Num | 19.6 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineNum |
| PERCONTROL | Yes | AbsEntry, DprArea, PeriodCat, VisOrder |
