# OITR - Internal Reconciliation

- **Tabla:** OITR
- **Descripción:** Internal Reconciliation
- **Cantidad de campos:** 30
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OITR.html

## Campos (30)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ReconNum` | Reconciliation Number | Int | 11 | - |  |  |
| 2 | `IsCard` | BP or Account | VarChar | 1 | - |  | `C` = BP<br>`A` = G/L Account |
| 3 | `ReconType` | Reconciliation Type | nVarChar | 2 | - |  | `0` = Manual<br>`1` = Automatic<br>`2` = Semi-Automatic<br>`3` = Payment<br>`4` = Credit Memo<br>`5` = Reversal<br>`6` = Zero Value<br>`7` = Cancellation<br>`8` = BoE<br>`9` = Deposit<br>`10` = Bank Statement Processing<br>`11` = Period Closing<br>`12` = Correction Invoice<br>`13` = Inventory/Expense Allocation<br>`14` = WIP<br>`15` = Deferred Tax Interim Account<br>`16` = Down Payment Allocation<br>`17` = Auto. Conversion Difference<br>`18` = Interim Document<br>`19` = Withholding Tax Interim Account<br>`20` = eTDS Posted to BP |
| 4 | `ReconDate` | Reconciliation Date | Date | 8 | - |  |  |
| 5 | `Total` | Total Reconciliation Amount | Num | 19.6 | - |  |  |
| 6 | `ReconCurr` | Reconciliation Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 7 | `Canceled` | Canceled | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `CancelAbs` | Canceling/-ed Reconciliation | Int | 11 | [OITR](OITR.md) | 0 |  |
| 9 | `IsSystem` | System or Manual | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 10 | `InitObjTyp` | Reconc. Initiator Object Type | nVarChar | 20 | - |  |  |
| 11 | `InitObjAbs` | Reconc. Initiator Internal ID | Int | 11 | - |  |  |
| 12 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 13 | `CreateTime` | Creation Time | Int | 6 | - |  |  |
| 14 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Auto Incr.<br>`D` = Data Doc.<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 15 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 16 | `ReconRule1` | Reconciliation Rule 1 | nVarChar | 2 | - |  | `0` = Posting Date<br>`1` = Due Date<br>`2` = Document Date<br>`3` = Ref. 1<br>`4` = Ref. 2<br>`5` = Ref. 3<br>`6` = Project Code<br>`7` = Control Account Code<br>`8` = Posting Period |
| 17 | `ReconRule2` | Reconciliation Rule 2 | nVarChar | 2 | - |  | `0` = Posting Date<br>`1` = Due Date<br>`2` = Document Date<br>`3` = Ref. 1<br>`4` = Ref. 2<br>`5` = Ref. 3<br>`6` = Project Code<br>`7` = Control Account Code<br>`8` = Posting Period |
| 18 | `ReconRule3` | Reconciliation Rule 3 | nVarChar | 2 | - |  | `0` = Posting Date<br>`1` = Due Date<br>`2` = Document Date<br>`3` = Ref. 1<br>`4` = Ref. 2<br>`5` = Ref. 3<br>`6` = Project Code<br>`7` = Control Account Code<br>`8` = Posting Period |
| 19 | `IsMultiBP` | Multiple BP Reconciliation | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 20 | `VersionNum` | Version Number | nVarChar | 13 | - |  |  |
| 21 | `OldMatNum` | Previous Reconciliation Number | Int | 11 | - | 0 |  |
| 22 | `ReconJEId` | JE no. created by reconciliatn | Int | 11 | - |  |  |
| 23 | `BuildDesc` | Build Descriptor | nVarChar | 50 | - |  |  |
| 24 | `BPLId` | Branch | Int | 11 | [OBPL](OBPL.md) |  |  |
| 25 | `BPLName` | Branch Name | nVarChar | 200 | - |  |  |
| 26 | `VATRegNum` | VAT Reg. Number | nVarChar | 32 | - |  |  |
| 27 | `IsElectr` | Is Electronic | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 28 | `CreateTS` | Creation Time - Incl. Sec. | Int | 11 | - |  |  |
| 29 | `UpdateTS` | Update Full Time | Int | 11 | - |  |  |
| 30 | `ObjType` | Object Type | nVarChar | 20 | - | 321 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ReconNum |
