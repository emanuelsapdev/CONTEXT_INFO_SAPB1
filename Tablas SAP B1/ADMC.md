# ADMC - G/L Account Determination Criteria - Inventory - History

- **Tabla:** ADMC
- **Descripción:** G/L Account Determination Criteria - Inventory - History
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ADMC.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DmcId` | Determination ID | Int | 6 | - |  |  |
| 2 | `DmcAlias` | Determination Alias | nVarChar | 100 | - |  |  |
| 3 | `Active` | Determination Status | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 4 | `Priority` | Determination Priority | Int | 6 | - |  |  |
| 5 | `LogInstanc` | Log Instance | Int | 11 | - |  |  |
| 6 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 7 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 8 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 9 | `AdvRulCol` | Advanced Rules Column | Int | 6 | - |  |  |
| 10 | `IsUDF` | Is User Defined Field | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DmcId, LogInstanc |
