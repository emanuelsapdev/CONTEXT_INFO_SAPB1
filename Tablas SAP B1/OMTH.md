# OMTH - Reconciliation History

- **Tabla:** OMTH
- **Descripción:** Reconciliation History
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OMTH.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `MthAcctCod` | Account Code | nVarChar | 15 | - |  |  |
| 2 | `IsInternal` | Reconciliation Type | VarChar | 1 | - | E | `I` = Internal<br>`E` = External |
| 3 | `MatchNum` | Reconciliation No. | Int | 11 | - |  |  |
| 4 | `Totals` | Recon. Amount (One Side) | Num | 19.6 | - |  |  |
| 5 | `IsCard` | Select BP or Account | VarChar | 1 | - | A | `A` = G/L Account<br>`C` = BP |
| 6 | `MatchType` | Reconciliation Type | nVarChar | 2 | - | 0 | `0` = Manual<br>`1` = Ref. 1<br>`2` = Ref. 2<br>`3` = Ref. 3<br>`4` = Posting Date<br>`5` = Due Date<br>`6` = Ref. 1 + Posting Date<br>`7` = Ref. 2 + Posting Date<br>`8` = Ref. 3 + Posting Date<br>`9` = Ref. 1 + Due Date<br>`10` = Ref. 2 + Due Date<br>`11` = Ref. 3 + Due Date<br>`12` = By Total |
| 7 | `TransId` | Reconciliation Transaction No. | Int | 11 | - | -1 |  |
| 8 | `MatchDate` | Reconciliation Date | Date | 8 | - |  |  |
| 9 | `CurrType` | Currency Type | nVarChar | 3 | - |  |  |
| 10 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 11 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 12 | `createDate` | Creation Date | Date | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | MthAcctCod, IsInternal, MatchNum |
