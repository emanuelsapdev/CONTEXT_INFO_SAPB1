# AEXT - Expense Types

- **Tabla:** AEXT
- **Descripción:** Expense Types
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AEXT.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ExpType` | Expense Type | nVarChar | 4 | - |  |  |
| 2 | `ExpName` | Expense Name | nVarChar | 30 | - |  |  |
| 3 | `ExpAcct` | G/L Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 4 | `PaidByComp` | Paid By Company | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 5 | `VatGroup` | VAT Group | nVarChar | 8 | [OSTC](OSTC.md) |  |  |
| 6 | `VatGrpEU` | VAT Group | nVarChar | 8 | [OVTG](OVTG.md) |  |  |
| 7 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 8 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 9 | `UpdateDate` | Update Date | Date | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ExpType, LogInstanc |
