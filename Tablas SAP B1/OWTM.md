# OWTM - Approval Templates

- **Tabla:** OWTM
- **Descripción:** Approval Templates
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OWTM.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WtmCode` | Code | Int | 11 | [OWTM](OWTM.md) |  |  |
| 2 | `Name` | Name | nVarChar | 20 | - |  |  |
| 3 | `Remarks` | Description | nVarChar | 100 | - |  |  |
| 4 | `Conds` | Conditions | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 5 | `Active` | Active | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 6 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 7 | `PmptChg` | Prompt Change | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 8 | `AppOnUpd` | Apply on Update | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WtmCode |
| NAME | Yes | Name |
