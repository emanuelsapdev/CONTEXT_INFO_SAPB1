# LGL1 - Legal Data - Rows

- **Tabla:** LGL1
- **Descripción:** Legal Data - Rows
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/LGL1.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal ID | Int | 11 | [OLGL](OLGL.md) |  |  |
| 2 | `LineSeq` | Line Sequence | Int | 11 | - |  |  |
| 3 | `LineType` | Line Type | VarChar | 1 | - | R | `T` = Document Total<br>`R` = Tax Per Line<br>`V` = Total Tax |
| 4 | `TaxCode` | Tax Code | nVarChar | 8 | - |  |  |
| 5 | `TaxRate` | Tax Rate | Num | 19.6 | - |  |  |
| 6 | `Amount` | Amount | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineSeq |
