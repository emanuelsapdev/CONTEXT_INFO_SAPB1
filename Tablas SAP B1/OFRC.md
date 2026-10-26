# OFRC - Financial Report Categories

- **Tabla:** OFRC
- **Descripción:** Financial Report Categories
- **Cantidad de campos:** 87
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OFRC.html

## Campos (87)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CatId` | Numerator | Int | 6 | - |  |  |
| 2 | `TemplateId` | Template | Int | 11 | [OFRT](OFRT.md) |  |  |
| 3 | `Name` | Name | nVarChar | 254 | - |  |  |
| 4 | `FrgnName` | Foreign Name | nVarChar | 254 | - |  |  |
| 5 | `Levels` | Account Level | Int | 6 | - | 1 | `1` = Level 1<br>`2` = Level 2<br>`3` = Level 3 |
| 6 | `FatherNum` | Parent Account Key | Int | 6 | - |  |  |
| 7 | `Active` | Active Account | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `HasSons` | Including Children | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 9 | `VisOrder` | Display Order | Int | 6 | - |  |  |
| 10 | `SubSum` | Subtotal | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 11 | `SubName` | Subtotal Name | nVarChar | 100 | - |  |  |
| 12 | `Furmula` | Formula | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 13 | `Param_1` | Parameter 1 | Int | 6 | - | 0 |  |
| 14 | `Param_2` | Parameter 2 | Int | 6 | - | 0 |  |
| 15 | `Param_3` | Parameter 3 | Int | 6 | - | 0 |  |
| 16 | `Param_4` | Parameter 4 | Int | 6 | - | 0 |  |
| 17 | `Param_5` | Parameter 5 | Int | 6 | - | 0 |  |
| 18 | `Param_6` | Parameter 6 | Int | 6 | - | 0 |  |
| 19 | `Param_7` | Parameter 7 | Int | 6 | - | 0 |  |
| 20 | `Param_8` | Parameter 8 | Int | 6 | - | 0 |  |
| 21 | `Param_9` | Parameter 9 | Int | 6 | - | 0 |  |
| 22 | `Param_10` | Parameter 10 | Int | 6 | - | 0 |  |
| 23 | `Param_11` | Parameter 11 | Int | 6 | - | 0 |  |
| 24 | `Param_12` | Parameter 12 | Int | 6 | - | 0 |  |
| 25 | `Param_13` | Parameter 13 | Int | 6 | - | 0 |  |
| 26 | `Param_14` | Parameter 14 | Int | 6 | - | 0 |  |
| 27 | `Param_15` | Parameter 15 | Int | 6 | - | 0 |  |
| 28 | `Param_16` | Parameter 16 | Int | 6 | - | 0 |  |
| 29 | `Param_17` | Parameter 17 | Int | 6 | - | 0 |  |
| 30 | `Param_18` | Parameter 18 | Int | 6 | - | 0 |  |
| 31 | `Param_19` | Parameter 19 | Int | 6 | - | 0 |  |
| 32 | `Param_20` | Parameter 20 | Int | 6 | - | 0 |  |
| 33 | `Param_21` | Parameter 21 | Int | 6 | - | 0 |  |
| 34 | `Param_22` | Parameter 22 | Int | 6 | - | 0 |  |
| 35 | `Param_23` | Parameter 23 | Int | 6 | - | 0 |  |
| 36 | `Param_24` | Parameter 24 | Int | 6 | - | 0 |  |
| 37 | `Param_25` | Parameter 25 | Int | 6 | - | 0 |  |
| 38 | `OP_1` | Operator 1 | VarChar | 1 | - |  | Without<br>`+` = Addition<br>`-` = Subtraction |
| 39 | `OP_2` | Operator 2 | VarChar | 1 | - |  | Without<br>`+` = Addition<br>`-` = Subtraction |
| 40 | `OP_3` | Operator 3 | VarChar | 1 | - |  | Without<br>`+` = Addition<br>`-` = Subtraction |
| 41 | `OP_4` | Operator 4 | VarChar | 1 | - |  | Without<br>`+` = Addition<br>`-` = Subtraction |
| 42 | `OP_5` | Operator 5 | VarChar | 1 | - |  | Without<br>`+` = Addition<br>`-` = Subtraction |
| 43 | `OP_6` | Operator 6 | VarChar | 1 | - |  | Without<br>`+` = Addition<br>`-` = Subtraction |
| 44 | `OP_7` | Operator 7 | VarChar | 1 | - |  | Without<br>`+` = Addition<br>`-` = Subtraction |
| 45 | `OP_8` | Operator 8 | VarChar | 1 | - |  | Without<br>`+` = Addition<br>`-` = Subtraction |
| 46 | `OP_9` | Operator 9 | VarChar | 1 | - |  | Without<br>`+` = Addition<br>`-` = Subtraction |
| 47 | `OP_10` | Operator 10 | VarChar | 1 | - |  | Without<br>`+` = Addition<br>`-` = Subtraction |
| 48 | `OP_11` | Operator 11 | VarChar | 1 | - |  | Without<br>`+` = Addition<br>`-` = Subtraction |
| 49 | `OP_12` | Operator 12 | VarChar | 1 | - |  | Without<br>`+` = Addition<br>`-` = Subtraction |
| 50 | `OP_13` | Operator 13 | VarChar | 1 | - |  | Without<br>`+` = Addition<br>`-` = Subtraction |
| 51 | `OP_14` | Operator 14 | VarChar | 1 | - |  | Without<br>`+` = Addition<br>`-` = Subtraction |
| 52 | `OP_15` | Operator 15 | VarChar | 1 | - |  | Without<br>`+` = Addition<br>`-` = Subtraction |
| 53 | `OP_16` | Operator 16 | VarChar | 1 | - |  | Without<br>`+` = Addition<br>`-` = Subtraction |
| 54 | `OP_17` | Operator 17 | VarChar | 1 | - |  | Without<br>`+` = Addition<br>`-` = Subtraction |
| 55 | `OP_18` | Operator 18 | VarChar | 1 | - |  | Without<br>`+` = Addition<br>`-` = Subtraction |
| 56 | `OP_19` | Operator 19 | VarChar | 1 | - |  | Without<br>`+` = Addition<br>`-` = Subtraction |
| 57 | `OP_20` | Operator 20 | VarChar | 1 | - |  | Without<br>`+` = Addition<br>`-` = Subtraction |
| 58 | `OP_21` | Operator 21 | VarChar | 1 | - |  | Without<br>`+` = Addition<br>`-` = Subtraction |
| 59 | `OP_22` | Operator 22 | VarChar | 1 | - |  | Without<br>`+` = Addition<br>`-` = Subtraction |
| 60 | `OP_23` | Operator 23 | VarChar | 1 | - |  | Without<br>`+` = Addition<br>`-` = Subtraction |
| 61 | `OP_24` | Operator 24 | VarChar | 1 | - |  | Without<br>`+` = Addition<br>`-` = Subtraction |
| 62 | `ProfitLoss` | Profit and Loss | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 63 | `MoveNeg` | Move if Negative | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 64 | `Dummy` | Dummy Title | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 65 | `HideAct` | Hide Accounts | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 66 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 67 | `ToGroup` | Move to Group | Int | 6 | - | 0 |  |
| 68 | `ToTitle` | Move to Title | Int | 6 | - | 0 |  |
| 69 | `LineNum` | Line Number | nVarChar | 6 | - |  |  |
| 70 | `IndentChar` | Indent Char. | nVarChar | 6 | - |  |  |
| 71 | `Reversal` | Reversal Sign | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 72 | `TextTitle` | Text Title | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 73 | `SumType` | Gross/Correction/Net | VarChar | 1 | - | N | `B` = Gross<br>`C` = Correction<br>`N` = Net |
| 74 | `NetIncome` | Net Income | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 75 | `PLTempId` | Profit & Loss Report Template | Int | 11 | - |  |  |
| 76 | `CustName` | Customized Account Name | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 77 | `ExtFromBS` | Relevant for Bal. Sht Extract | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 78 | `ExtData` | Extended Data | VarChar | 1 | - | N | `A` = Relevant for Asset History Sheet<br>`L` = Relevant for Liabilities History Sheet<br>`N` = Not Relevant |
| 79 | `LegalRef` | Legal Reference | nVarChar | 150 | - |  |  |
| 80 | `PLCatId` | Profit & Loss Report Category | Int | 6 | - | 0 |  |
| 81 | `SignAggr` | Sign for Aggregation | VarChar | 1 | - | E | `E`<br>`P` = Positive<br>`N` = Negative |
| 82 | `Mandatory` | Mandatory | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 83 | `AcctReq` | Account Verification Required | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 84 | `NotPermit` | Not Permitted for Tax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 85 | `KPIFactor` | KPI Factor No. | nVarChar | 3 | [OKPF](OKPF.md) |  |  |
| 86 | `CatCode` | Category Code | nVarChar | 15 | - |  |  |
| 87 | `CatClass` | Category Classification | VarChar | 1 | - |  | `A` = Asset<br>`L` = Liabilities<br>`E` = Equity<br>`D` = Expenses<br>`R` = Revenues |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TemplateId, CatId |
