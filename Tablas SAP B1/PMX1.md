# PMX1 - Payroll Line

- **Tabla:** PMX1
- **Descripción:** Payroll Line
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/PMX1.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [OPMX](OPMX.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `CateType` | Category Type | VarChar | 1 | - |  |  |
| 4 | `CateCode` | Category Code | nVarChar | 3 | - |  |  |
| 5 | `Keyword` | Keyword | nVarChar | 10 | - |  |  |
| 6 | `Category` | Category | nVarChar | 100 | - |  |  |
| 7 | `Debit` | Debit Amount | nVarChar | 20 | - |  |  |
| 8 | `Credit` | Credit Amout | nVarChar | 20 | - |  |  |
| 9 | `FCDebit` | FC Debit Amount | nVarChar | 20 | - |  |  |
| 10 | `FCCredit` | FC Credit Amount | nVarChar | 20 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineNum |
