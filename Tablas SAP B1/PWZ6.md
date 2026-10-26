# PWZ6 - Payment Wizard Rows - 6

- **Tabla:** PWZ6
- **Descripción:** Payment Wizard Rows - 6
- **Cantidad de campos:** 13
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/PWZ6.html

## Campos (13)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `IdEntry` | ID Number | Int | 11 | [OPWZ](OPWZ.md) |  |  |
| 2 | `CondNum` | Condition Number | Int | 11 | - |  |  |
| 3 | `SelFldID` | Selection Field ID | nVarChar | 100 | - |  |  |
| 4 | `FromString` | From String Value | nVarChar | 200 | - |  |  |
| 5 | `FromNumber` | From Number Value | Int | 11 | - |  |  |
| 6 | `FromMoney` | From Amount Value | Num | 19.6 | - |  |  |
| 7 | `FromDate` | From Date Value | Date | 8 | - |  |  |
| 8 | `FromMemo` | From Memo Value | Text | 16 | - |  |  |
| 9 | `ToString` | To String Value | nVarChar | 200 | - |  |  |
| 10 | `ToNumber` | To Number Value | Int | 11 | - |  |  |
| 11 | `ToMoney` | To Amount Value | Num | 19.6 | - |  |  |
| 12 | `ToDate` | To Date Value | Date | 8 | - |  |  |
| 13 | `ToMemo` | To Memo Value | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | IdEntry, CondNum |
