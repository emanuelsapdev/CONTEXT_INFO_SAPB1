# AADT - Fixed Assets Account Determination - History

- **Tabla:** AADT
- **Descripción:** Fixed Assets Account Determination - History
- **Cantidad de campos:** 29
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AADT.html

## Campos (29)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Code | nVarChar | 15 | - |  |  |
| 2 | `Descr` | Description | nVarChar | 100 | - |  |  |
| 3 | `BalanceAct` | Asset Balance Sheet Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 4 | `ClrAcqAct` | Acquisition Clearing Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 5 | `RevResvAct` | Revaluation Reserve | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 6 | `OrdDprAct` | Ordinary Depreciation | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 7 | `OrdDprAcc` | Accumulated Ordinary Depr. | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 8 | `UnpDprAct` | Unplanned Depreciation | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 9 | `UnpDprAcc` | Accumulated Unplanned Depr. | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 10 | `SpDprAct` | Special Depreciation | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 11 | `SpDprAcc` | Accumulated Special Depr. | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 12 | `SaRevNAct` | Revenue from Asset Sales (Net) | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 13 | `ReExpNAct` | Retirement with Expense (Net) | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 14 | `ReRevNAct` | Retirement with Revenue (Net) | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 15 | `ReNBVeAct` | NBV Retirement Expense (Gross) | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 16 | `ReNBVrAct` | NBV Retirement Revenue (Gross) | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 17 | `ClrDscAct` | Cash Discount Clearing Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 18 | `RevReAct` | Revenue Account for Retirement | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 19 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 20 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 21 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 22 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 23 | `UserSign2` | Updating User | Int | 6 | - |  |  |
| 24 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 25 | `ClearAccRe` | Revenue Clearing Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 26 | `RevResvClr` | Revaluation Reserve Clearing | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 27 | `SnapshotId` | Snapshot ID | Int | 11 | - | 0 |  |
| 28 | `RevAct` | Revaluation Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 29 | `RevLossAct` | Revaluation Loss | nVarChar | 15 | [OACT](OACT.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code, LogInstanc |
