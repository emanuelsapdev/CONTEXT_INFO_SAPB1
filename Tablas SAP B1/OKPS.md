# OKPS - KPI Set

- **Tabla:** OKPS
- **Descripción:** KPI Set
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OKPS.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `KpsCode` | KPI Set Code | nVarChar | 15 | - |  |  |
| 2 | `KpsName` | KPI Set Name | nVarChar | 100 | - |  |  |
| 3 | `KpsType` | KPI Set Type | VarChar | 1 | - | S | `S` = Single<br>`Q` = Quarterly<br>`M` = Monthly<br>`P` = Multiple |
| 4 | `FieldsNum` | KPI Set Fields Number | Int | 11 | - |  |  |
| 5 | `CreateDate` | Create Date - History | Date | 8 | - |  |  |
| 6 | `UserSign` | Updating User - History | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | KpsCode |
