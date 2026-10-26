# VLG1 - Validation of Recalc. From To

- **Tabla:** VLG1
- **Descripción:** Validation of Recalc. From To
- **Cantidad de campos:** 13
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/VLG1.html

## Campos (13)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Unique Key | Int | 11 | [IVLG](IVLG.md) |  |  |
| 2 | `RecNum` | Record Number | Int | 11 | - |  |  |
| 3 | `FromSysDat` | From System Date | Date | 8 | - |  |  |
| 4 | `FromDocNum` | From Document Number | Int | 11 | [OINM](OINM.md) |  |  |
| 5 | `FromDocTyp` | From Document Type | Int | 6 | - |  |  |
| 6 | `ToSysDate` | To System Date | Date | 8 | - |  |  |
| 7 | `ToDocNum` | To Document Number | Int | 11 | [OINM](OINM.md) |  |  |
| 8 | `ToDocType` | To Document Type | Int | 6 | - |  |  |
| 9 | `CalRecOINM` | Calculated Record in OINM | Int | 11 | - |  |  |
| 10 | `LastCalcTS` | Last Calculated Trans. Seq. | Int | 11 | - |  |  |
| 11 | `SumTranVal` | Sum of Transaction Value | Num | 19.6 | - |  |  |
| 12 | `StrFld` | General String Field | nVarChar | 50 | - |  |  |
| 13 | `NumFld` | General Number Field | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, RecNum |
