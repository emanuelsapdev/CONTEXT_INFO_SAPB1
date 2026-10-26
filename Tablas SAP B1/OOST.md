# OOST - Opportunity Stage

- **Tabla:** OOST
- **Descripción:** Opportunity Stage
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OOST.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Num` | Sequence No. | Int | 11 | - |  |  |
| 2 | `Descript` | Name | nVarChar | 30 | - |  |  |
| 3 | `StepId` | Stage No. | Int | 6 | - |  |  |
| 4 | `CloPrcnt` | Closing Percentage | Num | 19.6 | - |  |  |
| 5 | `Canceled` | Canceled | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 7 | `SalesStage` | Sales | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 8 | `PurStage` | Purchasing | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Num |
| STEP | Yes | StepId |
