# GBI1 - GBI Row 1 - Electronic Account Book

- **Tabla:** GBI1
- **Descripción:** GBI Row 1 - Electronic Account Book
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/GBI1.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `HistoryId` | History Key | Int | 11 | [OGBI](OGBI.md) |  |  |
| 2 | `RowId` | Row Number | Int | 11 | - |  |  |
| 3 | `AcctBkNo` | Electronic Account Book No. | nVarChar | 5 | - |  |  |
| 4 | `AcctBkName` | Electronic Account Book Name | nVarChar | 30 | - |  |  |
| 5 | `OrgCode` | Organizational Code | nVarChar | 20 | - |  |  |
| 6 | `CompType` | Company Type | nVarChar | 8 | - |  |  |
| 7 | `Industry` | Industry | nVarChar | 20 | - |  |  |
| 8 | `SoftVender` | Accounting Software Provider | nVarChar | 60 | - |  |  |
| 9 | `Version` | Accounting Software Version | nVarChar | 20 | - |  |  |
| 10 | `FisYear` | Fiscal Year | nVarChar | 4 | - |  |  |
| 11 | `LocCurr` | Local Currency | nVarChar | 3 | - |  |  |
| 12 | `AcctStruct` | Account Structure | nVarChar | 30 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | HistoryId, RowId |
