# DGP2 - Expanded Selection Criteria

- **Tabla:** DGP2
- **Descripción:** Expanded Selection Criteria
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/DGP2.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [ODGP](ODGP.md) |  |  |
| 2 | `CondNum` | Condition Number | Int | 11 | - |  |  |
| 3 | `SelFldID` | Selection Field ID | nVarChar | 100 | - |  |  |
| 4 | `FromString` | String Value From | nVarChar | 200 | - |  |  |
| 5 | `FromNumber` | Number Value From | Int | 11 | - |  |  |
| 6 | `FromMoney` | Amount Value From | Num | 19.6 | - |  |  |
| 7 | `FromDate` | Date Value From | Date | 8 | - |  |  |
| 8 | `ToString` | String Value To | nVarChar | 200 | - |  |  |
| 9 | `ToNumber` | Number Value To | Int | 11 | - |  |  |
| 10 | `ToMoney` | Amount Value To | Num | 19.6 | - |  |  |
| 11 | `ToDate` | Date Value To | Date | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, CondNum |
