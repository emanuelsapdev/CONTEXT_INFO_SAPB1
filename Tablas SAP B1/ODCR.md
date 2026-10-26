# ODCR - Checking Rule

- **Tabla:** ODCR
- **Descripción:** Checking Rule
- **Cantidad de campos:** 16
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ODCR.html

## Campos (16)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `RuleCode` | Checking Rule Code | nVarChar | 2 | - |  |  |
| 2 | `RuleDesc` | Checking Rule Description | nVarChar | 100 | - |  |  |
| 3 | `PastRcp` | Include Past Plan Receipts | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 4 | `AutoATP` | ATP Check Automatically | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 5 | `SLDUncfm` | Schedule for Unconfirmed Qty | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 6 | `AllowUncfm` | Allow Unconfirmed Quantity | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 7 | `CmltStrtg` | Cumulation Strategy | VarChar | 1 | - | R | `R` = Required Qty on Creation; Confirmed Qty on Change<br>`C` = Confirmed Qty on Creation and Change |
| 8 | `DeliStrtg` | Delivery Strategy | VarChar | 1 | - | D | `D` = Delivery Proposal<br>`O` = One-Time Delivery<br>`C` = Complete Delivery |
| 9 | `MaxPrpsls` | Max. No. of Proposals | Int | 11 | - | 9 |  |
| 10 | `validFor` | Active | VarChar | 1 | - | N |  |
| 11 | `validFrom` | Active From | nVarChar | 8 | - |  |  |
| 12 | `validTo` | Active To | nVarChar | 8 | - |  |  |
| 13 | `frozenFor` | Inactive | VarChar | 1 | - | N |  |
| 14 | `frozenFrom` | Inactive From | nVarChar | 8 | - |  |  |
| 15 | `frozenTo` | Inactive To | nVarChar | 8 | - |  |  |
| 16 | `Locked` | Locked | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | RuleCode |
