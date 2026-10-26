# OWMA - WTax Monthly Accumulation

- **Tabla:** OWMA
- **Descripción:** WTax Monthly Accumulation
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OWMA.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `CardCode` | BP Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 3 | `PeriodYear` | Accumulation Year | Int | 11 | - |  |  |
| 4 | `PerMonth` | Accumulation Month | Int | 11 | - |  |  |
| 5 | `WTTypeId` | WTax Type ID | Int | 11 | - |  |  |
| 6 | `BPLId` | Branch | Int | 11 | - | 0 |  |
| 7 | `AccumType` | Accumulation Type (P=Payment, I=Invoice) | VarChar | 1 | - |  |  |
| 8 | `WTCode` | WTax Code | nVarChar | 10 | - |  |  |
| 9 | `TxblAccm` | Taxable Accumulated Amount | Num | 19.6 | - |  |  |
| 10 | `WhtAccm` | WTax Accumulated Amount | Num | 19.6 | - |  |  |
| 11 | `WTCur` | WTax Currency | nVarChar | 10 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| SECONDARY | Yes | CardCode, PeriodYear, PerMonth, WTCode, BPLId, AccumType |
