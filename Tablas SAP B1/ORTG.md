# ORTG - Deducted Tax Definition

- **Tabla:** ORTG
- **Descripción:** Deducted Tax Definition
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ORTG.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Code | nVarChar | 8 | - |  |  |
| 2 | `Name` | Name | nVarChar | 50 | - |  |  |
| 3 | `Inactive` | Inactive | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 4 | `Category` | Category | VarChar | 1 | - | I | `I` = Input Tax |
| 5 | `RecognRate` | Deducted Purchase Tax % | Num | 19.6 | - |  |  |
| 6 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 7 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 8 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 9 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 10 | `IsSystem` | System Deducted Tax Code | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code |
| GROUP_NAME | No | Name |
