# DGP5 - Sort By List

- **Tabla:** DGP5
- **Descripción:** Sort By List
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/DGP5.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [ODGP](ODGP.md) |  |  |
| 2 | `CondNum` | Condition Number | Int | 11 | - |  |  |
| 3 | `SortField` | Sort Field | nVarChar | 100 | - | DocNum | `-1`<br>`DocNum` = Document Number<br>`DocDate` = Posting Date<br>`DocDueDate` = Due Date<br>`NumAtCard` = BP Reference No.<br>`DocTotal` = Document Amount<br>`SlpCode` = Sales Employee |
| 4 | `SortOrder` | Sort Order | VarChar | 1 | - | A | `A` = Ascending<br>`D` = Descending |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, CondNum |
