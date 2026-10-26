# OIWZ - Inflation Wizard

- **Tabla:** OIWZ
- **Descripción:** Inflation Wizard
- **Cantidad de campos:** 36
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OIWZ.html

## Campos (36)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `WizName` | Wizard Name | nVarChar | 100 | - |  |  |
| 3 | `PostDateTo` | Posting Date To | Date | 8 | - |  |  |
| 4 | `WizType` | Wizard Type | VarChar | 1 | - |  | `1` = G\L Account Revaluation Wizard<br>`2` = Inventory Revaluation Wizard<br>`3` = COGS Revaluation Wizard |
| 5 | `IndexCode` | Index Code | nVarChar | 3 | - |  |  |
| 6 | `IndexRate` | Index Rate | Num | 19.6 | - |  |  |
| 7 | `CashAcct` | Cash Account | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 8 | `CashFrmBl` | Cash from Balance | Num | 19.6 | - |  |  |
| 9 | `CashCancel` | Cash Cancel | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 10 | `FromItem` | Item Number To | nVarChar | 50 | - |  |  |
| 11 | `ToItem` | Item Number To | nVarChar | 50 | - |  |  |
| 12 | `ItemGroup` | Item Group | Int | 6 | - |  |  |
| 13 | `Properties` | Item Properties | nVarChar | 250 | - |  |  |
| 14 | `RvalMethod` | Inventory Revaluation Method | VarChar | 1 | - | P | `P` = Price Source<br>`I` = Inflation Only |
| 15 | `PriceSour` | Price Source | Int | 6 | - |  |  |
| 16 | `TransAbs` | Journal Entry Absolute Entry | Int | 11 | - |  |  |
| 17 | `UseDLN` | Use Delivery Notes | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 18 | `UsePCH` | Use Invoices with Stock Trans. | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 19 | `UsePCHNoSt` | Use Invoices without Trans. | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 20 | `UseImport` | Use Import Data | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 21 | `CashDifBal` | Cash Acct Difference Balance | Num | 19.6 | - |  |  |
| 22 | `CashExecut` | Cash Executed | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 23 | `ActType` | Account Type | VarChar | 1 | - | A | `A` = Post amount to adjustment account<br>`S` = Post amount to inventory account |
| 24 | `VarRate` | Price Variance Rate | Num | 19.6 | - |  |  |
| 25 | `FilterExe` | Filter Executed | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 26 | `CashErrRes` | Cash Account Error Reason | Int | 11 | - |  |  |
| 27 | `CshRvToAct` | Cash Revaluate to Account | nVarChar | 15 | - |  |  |
| 28 | `MarkVar` | Mark Items with Varient Price | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 29 | `ChngPrice` | Change Price | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 30 | `UseSemestr` | Revaluate by Semesters Index | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 31 | `CreateDate` | Create Date | Date | 8 | - |  |  |
| 32 | `CshLstRvBl` | Cash Last Revaluation Balance | Num | 19.6 | - |  |  |
| 33 | `userSign` | Creating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 34 | `userSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 35 | `CshCanclD` | Cash Acct Cancellation Date | Date | 8 | - |  |  |
| 36 | `BPLId` | Active Branch | Int | 11 | [OBPL](OBPL.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
