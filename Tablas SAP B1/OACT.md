# OACT - G/L Accounts

- **Tabla:** OACT
- **Descripción:** G/L Accounts
- **Cantidad de campos:** 131
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OACT.html

## Campos (131)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AcctCode` | Account Code | nVarChar | 15 | - |  |  |
| 2 | `AcctName` | Account Name | nVarChar | 200 | - |  |  |
| 3 | `CurrTotal` | Current Balance | Num | 19.6 | - |  |  |
| 4 | `EndTotal` | Opening Balance | Num | 19.6 | - |  |  |
| 5 | `Finanse` | Cash Account | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `Groups` | Main Group | nVarChar | 8 | - |  |  |
| 7 | `Budget` | Budget | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `Frozen` | Account on Hold [Y/N] | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 9 | `Free_2` | Free 2 | VarChar | 1 | - |  |  |
| 10 | `Postable` | Account [Active/Title] | VarChar | 1 | - | Y | `Y` = Active Account<br>`N` = Title Account |
| 11 | `Fixed` | Main Account | VarChar | 1 | - |  |  |
| 12 | `Levels` | Account Level | Int | 6 | - | 2 |  |
| 13 | `ExportCode` | Data Export Code | nVarChar | 10 | - |  |  |
| 14 | `GrpLine` | Serial No. in Group | Int | 11 | - |  |  |
| 15 | `FatherNum` | Parent Account Key | nVarChar | 15 | - |  |  |
| 16 | `AccntntCod` | External Code | nVarChar | 15 | - |  |  |
| 17 | `CashBox` | Capital Account [Y/N] | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 18 | `GroupMask` | Group Mask | Int | 6 | - | 1 |  |
| 19 | `RateTrans` | For Conversion Differences | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 20 | `TaxIncome` | Tax Definition | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 21 | `ExmIncome` | Tax Definition | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 22 | `ExtrMatch` | External Reconciliation No. | Int | 11 | - |  |  |
| 23 | `IntrMatch` | Internal Reconciliation No. | Int | 11 | - |  |  |
| 24 | `ActType` | Account Type | VarChar | 1 | - | N | `I` = Sales<br>`E` = Expenditure<br>`N` = Other |
| 25 | `Transfered` | Year Transfer [Y/N] | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 26 | `BlncTrnsfr` | Balances Transferred [Y/N] | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 27 | `OverType` | Loading Type | VarChar | 1 | - | N | `N` = None<br>`Y` = Yes |
| 28 | `OverCode` | Loading Factor Code | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 29 | `SysMatch` | System Reconciliation No. | Int | 11 | - | -1 |  |
| 30 | `PrevYear` | There are accounts from the previous year | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 31 | `ActCurr` | Account Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 32 | `RateDifAct` | Rate Differences Account | nVarChar | 15 | - |  |  |
| 33 | `SysTotal` | Balance in System Currency | Num | 19.6 | - |  |  |
| 34 | `FcTotal` | Balance in Account Currency | Num | 19.6 | - |  |  |
| 35 | `Protected` | Confidential Account | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 36 | `RealAcct` | Indexed Account | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 37 | `Advance` | Advance Payments | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 38 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 39 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 40 | `FrgnName` | Foreign Name | nVarChar | 200 | - |  |  |
| 41 | `Details` | Details | nVarChar | 254 | - |  |  |
| 42 | `ExtraSum` | Additional Amount | Num | 19.6 | - |  |  |
| 43 | `Project` | Project Code | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 44 | `RevalMatch` | Revaluation Coordinated | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 45 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 46 | `LocMth` | LC Reconciliation | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 47 | `MTHCounter` | MTH Counter | Int | 11 | - |  |  |
| 48 | `BNKCounter` | BNK Counter | Int | 11 | - |  |  |
| 49 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 50 | `LocManTran` | Control Account | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 51 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 52 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 1 |  |
| 53 | `ValidFor` | Active | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 54 | `ValidFrom` | Active From | Date | 8 | - |  |  |
| 55 | `ValidTo` | Active To | Date | 8 | - |  |  |
| 56 | `ValidComm` | Active Remarks | nVarChar | 30 | - |  |  |
| 57 | `FrozenFor` | Inactive | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 58 | `FrozenFrom` | Inactive From | Date | 8 | - |  |  |
| 59 | `FrozenTo` | Inactive To | Date | 8 | - |  |  |
| 60 | `FrozenComm` | Inactive Remarks | nVarChar | 30 | - |  |  |
| 61 | `Counter` | Counter | Int | 11 | - | 0 |  |
| 62 | `Segment_0` | Segment 0 | nVarChar | 20 | - |  |  |
| 63 | `Segment_1` | Segment 1 | nVarChar | 20 | - |  |  |
| 64 | `Segment_2` | Segment 2 | nVarChar | 20 | - |  |  |
| 65 | `Segment_3` | Segment 3 | nVarChar | 20 | - |  |  |
| 66 | `Segment_4` | Segment 4 | nVarChar | 20 | - |  |  |
| 67 | `Segment_5` | Segment 5 | nVarChar | 20 | - |  |  |
| 68 | `Segment_6` | Segment 6 | nVarChar | 20 | - |  |  |
| 69 | `Segment_7` | Segment 7 | nVarChar | 20 | - |  |  |
| 70 | `Segment_8` | Segment 8 | nVarChar | 20 | - |  |  |
| 71 | `Segment_9` | Segment 9 | nVarChar | 20 | - |  |  |
| 72 | `FormatCode` | Format Code | nVarChar | 210 | - |  |  |
| 73 | `CfwRlvnt` | Cash Flow Relevant [Y/N] | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 74 | `ExchRate` | Exchange Rate Differences | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 75 | `RevalAcct` | Revaluation Account | nVarChar | 15 | - |  |  |
| 76 | `LastRevBal` | Last Revaluation Balance | Num | 19.6 | - |  |  |
| 77 | `LastRevDat` | Last Revaluation Date | Date | 8 | - |  |  |
| 78 | `DfltVat` | Default VAT Group | nVarChar | 8 | [OVTG](OVTG.md) |  |  |
| 79 | `VatChange` | Allow Change VAT Group | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 80 | `Category` | Category | Int | 11 | [OACG](OACG.md) |  |  |
| 81 | `TransCode` | Transaction Code | nVarChar | 4 | [OTRC](OTRC.md) |  |  |
| 82 | `OverCode5` | Loading Factor Code 5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 83 | `OverCode2` | Loading Factor Code 2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 84 | `OverCode3` | Loading Factor Code 3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 85 | `OverCode4` | Loading Factor Code 4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 86 | `DfltTax` | Default Tax Code | nVarChar | 8 | [OSTC](OSTC.md) |  |  |
| 87 | `TaxPostAcc` | Default Tax Posting Account | VarChar | 1 | - | N | `N`<br>`R` = Sales Tax Account<br>`P` = Purchasing Tax Account |
| 88 | `AcctStrLe` | Account Structure Level | nVarChar | 2 | - |  |  |
| 89 | `MeaUnit` | Measurement Unit | nVarChar | 10 | - |  |  |
| 90 | `BalDirect` | Direction of Balance | nVarChar | 4 | - | 0 | `0`<br>`1` = Credit<br>`2` = Debit |
| 91 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 92 | `PlngLevel` | B1i Info for Integration | nVarChar | 2 | - |  |  |
| 93 | `MultiLink` | Allow Multiple Linking | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 94 | `PrjRelvnt` | Project Relevant | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 95 | `Dim1Relvnt` | Dimension 1 Relevant | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 96 | `Dim2Relvnt` | Dimension 2 Relevant | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 97 | `Dim3Relvnt` | Dimension 3 Relevant | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 98 | `Dim4Relvnt` | Dimension 4 Relevant | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 99 | `Dim5Relvnt` | Dimension 5 Relevant | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 100 | `AccrualTyp` | Accrual Type | VarChar | 1 | - | N | `N` = None<br>`P` = Posting Account<br>`C` = Calculation Account<br>`I` = Calculation Interim Account |
| 101 | `DatevAcct` | DATEV Account | nVarChar | 8 | - |  |  |
| 102 | `DatevAutoA` | DATEV Automatic Account | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 103 | `DatevFirst` | First Data Entry | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 104 | `SnapShotId` | Snapshot ID | Int | 11 | - | 0 |  |
| 105 | `PCN874Rpt` | PCN 874 Report Relevant | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 106 | `SCAdjust` | SC Adjustment | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 107 | `BPLId` | Assigned Branch | Int | 11 | [OBPL](OBPL.md) |  |  |
| 108 | `BPLName` | Branch Name | nVarChar | 200 | - |  |  |
| 109 | `SubLedgerN` | Subledger No. | nVarChar | 60 | - |  |  |
| 110 | `VATRegNum` | VAT Reg. Number | nVarChar | 32 | - |  |  |
| 111 | `ActId` | Account Identifier | nVarChar | 210 | - |  |  |
| 112 | `ClosingAcc` | G/L Account Closing | nVarChar | 15 | - |  |  |
| 113 | `PurpCode` | Account Purpose Code | nVarChar | 2 | - |  | `01` = Contas de ativo<br>`02` = Contas de Passivo<br>`03` = Patrim�nio L�quido<br>`04` = Contas de Resultado<br>`05` = Contas de Compensa��o<br>`09` = Outras |
| 114 | `RefCode` | Referential Account Code | nVarChar | 30 | - |  |  |
| 115 | `BlocManPos` | Block Manual Posting | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 116 | `PriAccCode` | Primary Closing Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 117 | `CstAccOnly` | Cost Account Only | VarChar | 1 | - | N | `Y` = YES<br>`N` = NO |
| 118 | `AlloweFrom` | Account Balance Allowed From | Num | 19.6 | - |  |  |
| 119 | `AllowedTo` | Account Balance Allowed To | Num | 19.6 | - |  |  |
| 120 | `BalanceA` | Account Balance Allowed | VarChar | 1 | - | N | `N` = NO<br>`Y` = YES |
| 121 | `RmrkTmpt` | Remark Text Template | Int | 11 | [OTTR](OTTR.md) |  |  |
| 122 | `CemRelvnt` | Cost Element Relevant | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 123 | `CemCode` | Cost Element Code | nVarChar | 20 | [OCEM](OCEM.md) |  |  |
| 124 | `StdActCode` | Standard Account Code | nVarChar | 35 | - |  |  |
| 125 | `TaxonCode` | Taxonomy Code | nVarChar | 15 | - |  |  |
| 126 | `InClassTyp` | Income Class. Type | Int | 11 | [OICP](OICP.md) |  |  |
| 127 | `InClassCat` | Income Class. Category | Int | 11 | [OICC](OICC.md) |  |  |
| 128 | `ExClassTyp` | Expense Class. Type | Int | 11 | [OECP](OECP.md) |  |  |
| 129 | `ExClassCat` | Expense Class. Category | Int | 11 | [OECC](OECC.md) |  |  |
| 130 | `OffcCode` | Official Account Code | nVarChar | 15 | - |  |  |
| 131 | `EUBPRelvnt` | euBP-Relevant | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (6)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AcctCode |
| INTER_KEY | No | FatherNum |
| CURRENCY | No | ActCurr |
| FORMAT | No | FormatCode |
| COUNTER | No | Counter |
| IDENTIFIER | Yes | ActId |
