# OSCM - Special Ledger - Analytical Accounting Configuration Rules: Material

- **Tabla:** OSCM
- **Descripción:** Special Ledger - Analytical Accounting Configuration Rules: Material
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSCM.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `RuleID` | Rule Identification Number | Int | 6 | - |  |  |
| 2 | `RuleType` | Rule Type Number | Int | 6 | - | 2 |  |
| 3 | `ParentID` | Parent Rule ID | Int | 6 | [OSCM](OSCM.md) |  |  |
| 4 | `Status` | Rule Status | VarChar | 1 | - |  |  |
| 5 | `Priority` | Rule Priority | Int | 6 | - | 100 |  |
| 6 | `Name` | Rule Name | nVarChar | 100 | - |  |  |
| 7 | `CreateDate` | Date of Rule Generation | Date | 8 | - |  |  |
| 8 | `UpdateDate` | Date of Rule Change | Date | 8 | - |  |  |
| 9 | `UserSign` | Rule Created By | Int | 6 | [OUSR](OUSR.md) |  |  |
| 10 | `UserSign2` | Rule Changed By | Int | 6 | [OUSR](OUSR.md) |  |  |
| 11 | `ExtCond` | Extended Special Data | nVarChar | 200 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | RuleID |
