# OACR - Accrual Type

- **Tabla:** OACR
- **Descripción:** Accrual Type
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OACR.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Accrual Type Code | nVarChar | 8 | - |  |  |
| 2 | `Name` | Accrual Type Name | nVarChar | 30 | - |  |  |
| 3 | `PostingAct` | Posting Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 4 | `CalcAcct` | Calculation Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 5 | `InterimAct` | Interim Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 6 | `Locked` | Locked | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 7 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 8 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code |
