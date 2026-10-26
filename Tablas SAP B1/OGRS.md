# OGRS - G/L Account Advanced Rules for Resources

- **Tabla:** OGRS
- **Descripción:** G/L Account Advanced Rules for Resources
- **Cantidad de campos:** 55
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OGRS.html

## Campos (55)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `PeriodCat` | Period Category | nVarChar | 10 | - |  |  |
| 3 | `FinancYear` | Beginning of Financial Year | Date | 8 | - |  |  |
| 4 | `Year` | Financial Year | Int | 6 | - |  |  |
| 5 | `PeriodName` | Period Name | nVarChar | 20 | - |  |  |
| 6 | `SubType` | Sub-Period Type | VarChar | 1 | - | Y | `Y` = Year<br>`Q` = Quarters<br>`M` = Months<br>`D` = Days |
| 7 | `PeriodNum` | Number of Periods | Int | 11 | - |  |  |
| 8 | `F_RefDate` | Posting Date From | Date | 8 | - |  |  |
| 9 | `T_RefDate` | Posting Date To | Date | 8 | - |  |  |
| 10 | `F_DueDate` | Due Date From | Date | 8 | - |  |  |
| 11 | `T_DueDate` | Due Date To | Date | 8 | - |  |  |
| 12 | `F_TaxDate` | Document Date From | Date | 8 | - |  |  |
| 13 | `T_TaxDate` | Document Date To | Date | 8 | - |  |  |
| 14 | `LogInstanc` | Log Instance | Int | 11 | - |  |  |
| 15 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 16 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 17 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 18 | `ResCode` | Resource No. | nVarChar | 50 | [ORSC](ORSC.md) |  |  |
| 19 | `ResGrpCod` | Resource Group | Int | 6 | [ORSB](ORSB.md) |  |  |
| 20 | `WhsCode` | Warehouse Code | nVarChar | 8 | - |  |  |
| 21 | `BPGrpCod` | BP Group | Int | 6 | - |  |  |
| 22 | `LicTradNum` | Federal Tax ID | nVarChar | 32 | - | !^\| | `!^\|` = All<br>`!^\|E` = Empty<br>`!^\|F` = Filled<br>`Enter Tax ID` = Enter Tax ID |
| 23 | `ShipCountr` | Ship-to Country/Region | nVarChar | 3 | - |  |  |
| 24 | `ShipState` | Ship-To State | nVarChar | 3 | - |  |  |
| 25 | `Comments` | Remarks | nVarChar | 254 | - |  |  |
| 26 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 27 | `RuleCode` | Advanced Rule Code | nVarChar | 20 | - |  |  |
| 28 | `GLMethod` | Get G/L Account By | VarChar | 1 | - | A | `A` = General<br>`W` = Warehouse<br>`C` = Resource Group |
| 29 | `Transfered` | Year Transfer [Y/N] | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 30 | `FromDate` | From Date | Date | 8 | - |  |  |
| 31 | `ToDate` | To Date | Date | 8 | - |  |  |
| 32 | `ResRevAct` | Resource Revenue Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 33 | `ResExpAct` | Resource Expense Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 34 | `ResSaleAct` | Resource Sales Credit Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 35 | `ResPurAct` | Resource Purchase Credit Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 36 | `ResNInvAct` | Resource Received Not Inv. Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 37 | `ResStdExp1` | Resource Std. Cost Expense 1 | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 38 | `ResStdExp2` | Resource Std. Cost Expense 2 | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 39 | `ResStdExp3` | Resource Std. Cost Expense 3 | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 40 | `ResStdExp4` | Resource Std. Cost Expense 4 | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 41 | `ResStdExp5` | Resource Std. Cost Expense 5 | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 42 | `ResStdExp6` | Resource Std. Cost Expense 6 | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 43 | `ResStdExp7` | Resource Std. Cost Expense 7 | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 44 | `ResStdExp8` | Resource Std. Cost Expense 8 | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 45 | `ResStdExp9` | Resource Std. Cost Expense 9 | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 46 | `ResStdEx10` | Resource Std. Cost Expense 10 | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 47 | `ResWipAct` | Resource WIP Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 48 | `ResScrapAc` | Scrap Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 49 | `WipOffPlAc` | WIP Offset P&L Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 50 | `ResOffPlAc` | Resource Offset P&L Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 51 | `Active` | Is Rule Active | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 52 | `CmpPrivate` | Company/Private | VarChar | 1 | - | A | `A` = All<br>`C` = Company<br>`I` = Private |
| 53 | `VatGroup` | Tax Definition | nVarChar | 8 | [OVTG](OVTG.md) |  |  |
| 54 | `CardCode` | Customer/Vendor Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 55 | `Usage` | Usage Code for Document | Int | 11 | [OUSG](OUSG.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
