# OPYD - Payment Run

- **Tabla:** OPYD
- **Descripción:** Payment Run
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OPYD.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Payment Run Code | nVarChar | 20 | - |  |  |
| 2 | `Name` | Payment Run Name | nVarChar | 50 | - |  |  |
| 3 | `TolerDays` | Tolerance Days | Int | 6 | - |  |  |
| 4 | `MinCashDis` | Min. Cash Discount | Num | 19.6 | - |  |  |
| 5 | `UseMinPay` | Use Minimum Payment | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `MinPayAR` | Minimum Incoming Payment | Num | 19.6 | - |  |  |
| 7 | `MinPayAP` | Minimum Outgoing Payment | Num | 19.6 | - |  |  |
| 8 | `ArePayMeth` | Payment Terms | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code |
