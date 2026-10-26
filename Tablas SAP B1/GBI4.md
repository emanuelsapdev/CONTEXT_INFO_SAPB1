# GBI4 - GBI Row 4 - Business Partners

- **Tabla:** GBI4
- **Descripción:** GBI Row 4 - Business Partners
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/GBI4.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `HistoryId` | History Key | Int | 11 | [OGBI](OGBI.md) |  |  |
| 2 | `RowId` | Row Number | Int | 11 | - |  |  |
| 3 | `BPNo` | BP Number | nVarChar | 30 | - |  |  |
| 4 | `BPName` | BP Name | nVarChar | 200 | - |  |  |
| 5 | `CatNo` | Category Number | Int | 6 | - |  |  |
| 6 | `Loc` | Location Area | nVarChar | 103 | - |  |  |
| 7 | `Tel` | Telephone | nVarChar | 50 | - |  |  |
| 8 | `Address` | Street/PO Box | nVarChar | 100 | - |  |  |
| 9 | `CreditRank` | Credit Rank | nVarChar | 6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | HistoryId, RowId |
