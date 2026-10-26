# OBOX - Box Definition

- **Tabla:** OBOX
- **Descripción:** Box Definition
- **Cantidad de campos:** 17
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OBOX.html

## Campos (17)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `BoxCode` | Code | nVarChar | 30 | - |  |  |
| 2 | `BoxName` | Name | nVarChar | 250 | - |  |  |
| 3 | `BoxType` | Type | VarChar | 1 | - | V | `V` = VAT Group<br>`B` = Box<br>`A` = Account<br>`M` = Manual Input<br>`T` = Manual Text Input<br>`F` = Formula<br>`S` = Single Choice |
| 4 | `SummayFld` | Summary Field | VarChar | 1 | - | S | `B` = Base Amount<br>`T` = Tax Amount<br>`Q` = EQ Base Amount<br>`E` = EQ Tax Amount<br>`N` = Non-Deductible Amount<br>`S` |
| 5 | `DbtCrdt` | Debit/Credit | VarChar | 1 | - | S | `D` = Debit Side<br>`C` = Credit Side<br>`B` = Debit Side and Credit Side<br>`S` |
| 6 | `Formula` | Formula Syntax | Text | 16 | - |  |  |
| 7 | `SortOrder` | Sort Order | Int | 11 | - |  |  |
| 8 | `AbsolutVa` | Absolute Value | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 9 | `ReportType` | Report Type | VarChar | 1 | - | B | `B` = Box Declaration<br>`S` = BAS Report<br>`X` = BAS Report - Empty Effective Date Holder |
| 10 | `Inactive` | Inactive | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 11 | `EffecDate` | Effective From | Date | 8 | - |  |  |
| 12 | `DecLoc` | Declaration Location | VarChar | 1 | - | B | `B`<br>`C` = Continent<br>`M` = Madeira<br>`A` = Azores |
| 13 | `BosCode` | Box Set Code | Int | 11 | [OBOS](OBOS.md) |  |  |
| 14 | `Position` | Position in Report | nVarChar | 250 | - |  |  |
| 15 | `PostToAct` | Post-To Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 16 | `PostToOffA` | Post-To Offset Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 17 | `Remarks` | Remarks | nVarChar | 254 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | BoxCode, ReportType, BosCode |
