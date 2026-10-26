# FAR1 - Fixed Asset Revaluation - Rows

- **Tabla:** FAR1
- **Descripción:** Fixed Asset Revaluation - Rows
- **Cantidad de campos:** 20
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/FAR1.html

## Campos (20)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | [OFAR](OFAR.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `ItemCode` | Item Code | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 4 | `NBV` | NBV | Num | 19.6 | - |  |  |
| 5 | `New_NBV` | New NBV | Num | 19.6 | - |  |  |
| 6 | `Remarks` | Remarks | nVarChar | 100 | - |  |  |
| 7 | `RevalPerc` | Revaluation Percentage % | Num | 19.6 | - |  |  |
| 8 | `OrdDprDur` | Ordinary Depr. During Period | Num | 19.6 | - |  |  |
| 9 | `UnDpDur` | Unplanned Depr. During Period | Num | 19.6 | - |  |  |
| 10 | `SpDprDur` | Special Depr. During Period | Num | 19.6 | - |  |  |
| 11 | `WriteUpDur` | Write-Up During Period | Num | 19.6 | - |  |  |
| 12 | `RevLossDur` | Revaluation Loss During Period | Num | 19.6 | - |  |  |
| 13 | `ReserveDur` | Reserve During Period | Num | 19.6 | - |  |  |
| 14 | `OcrCode` | Distribution Rule | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 15 | `OcrCode2` | Distribution Rule 2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 16 | `OcrCode3` | Distribution Rule 3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 17 | `OcrCode4` | Distribution Rule 4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 18 | `OcrCode5` | Distribution Rule 5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 19 | `Project` | Project Code | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 20 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum |
