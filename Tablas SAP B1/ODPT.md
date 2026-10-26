# ODPT - Postdated Deposit

- **Tabla:** ODPT
- **Descripción:** Postdated Deposit
- **Cantidad de campos:** 37
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ODPT.html

## Campos (37)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DeposId` | Payment Internal ID | Int | 11 | - | 0 |  |
| 2 | `DeposType` | Payment Type | VarChar | 1 | - | K | `K` = Check Deposit<br>`V` = Credit Deposit |
| 3 | `DeposDate` | Payment Date | Date | 8 | - |  |  |
| 4 | `DeposCurr` | Currency for Payments | nVarChar | 3 | - |  |  |
| 5 | `BanckAcct` | SAP Business One Acct Code f. | nVarChar | 15 | - |  |  |
| 6 | `Memo` | Details | nVarChar | 254 | - |  |  |
| 7 | `LocTotal` | Total (LC) | Num | 19.6 | - |  |  |
| 8 | `FcTotal` | Total (FC) | Num | 19.6 | - |  |  |
| 9 | `SysTotal` | Total (SC) | Num | 19.6 | - |  |  |
| 10 | `TransAbs` | Journal Entry Key | Int | 11 | [OJDT](OJDT.md) |  |  |
| 11 | `Ref1` | Reference 1 | nVarChar | 11 | - |  |  |
| 12 | `Ref2` | Reference 2 | nVarChar | 11 | - |  |  |
| 13 | `DocRate` | Payment Rate | Num | 19.6 | - |  |  |
| 14 | `Splited` | Split | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 15 | `VatAct` | Tax Account | nVarChar | 15 | - |  |  |
| 16 | `ComissAct` | Commissions Account | nVarChar | 15 | - |  |  |
| 17 | `VatTotal` | Total Tax | Num | 19.6 | - |  |  |
| 18 | `Comission` | Commission | Num | 19.6 | - |  |  |
| 19 | `ComissDate` | Commission Date | Date | 8 | - |  |  |
| 20 | `TaxDate` | Document Date | Date | 8 | - |  |  |
| 21 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 22 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) |  |  |
| 23 | `FinncPriod` | Posting Period | Int | 11 | [OFPR](OFPR.md) |  |  |
| 24 | `VatTotlSys` | Total Tax on Input (SC) | Num | 19.6 | - |  |  |
| 25 | `ComissnSys` | Total Commission (SC) | Num | 19.6 | - |  |  |
| 26 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 27 | `CommisVat` | Commission VAT Group | nVarChar | 8 | [OVTG](OVTG.md) |  |  |
| 28 | `Project` | Project Code | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 29 | `OcrCode` | Distribution Rule | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 30 | `OcrCode2` | Distribution Rule 2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 31 | `OcrCode3` | Distribution Rule 3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 32 | `OcrCode4` | Distribution Rule 4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 33 | `OcrCode5` | Distribution Rule 5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 34 | `ComisFC` | Total Commission (FC) | Num | 19.6 | - |  |  |
| 35 | `VatTotlFC` | Total Tax on Input (FC) | Num | 19.6 | - |  |  |
| 36 | `ComisCurr` | Commission Currency | nVarChar | 3 | - |  |  |
| 37 | `VersionNum` | Version Number | nVarChar | 13 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DeposId |
