# CFH1 - Cash Flow Statement Report - History - Rows

- **Tabla:** CFH1
- **Descripción:** Cash Flow Statement Report - History - Rows
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CFH1.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CFHId` | Cash Flow History Identity | Int | 11 | [OCFH](OCFH.md) |  |  |
| 2 | `LineId` | Row Number | Int | 11 | - |  |  |
| 3 | `DispItem` | Displayed Item Title | nVarChar | 100 | - |  |  |
| 4 | `Levels` | Levels | Int | 6 | - |  |  |
| 5 | `LineNum` | Cash Flow Line No. | nVarChar | 5 | - |  |  |
| 6 | `IndentChar` | Indent Char. | nVarChar | 6 | - | 4 |  |
| 7 | `Amount` | Amount | Num | 19.6 | - |  |  |
| 8 | `Formula` | Formula Flag | VarChar | 1 | - | N | `N` = Non-Formula<br>`Y` = Formula Node |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CFHId, LineId |
