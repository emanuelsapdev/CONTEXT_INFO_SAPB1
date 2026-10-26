# ORCR - Recurring Postings

- **Tabla:** ORCR
- **Descripción:** Recurring Postings
- **Cantidad de campos:** 26
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ORCR.html

## Campos (26)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `RcurCode` | Recurring Postings Code | nVarChar | 8 | - |  |  |
| 2 | `RcurDesc` | Transaction Description | nVarChar | 50 | - |  |  |
| 3 | `Frequency` | Frequency | VarChar | 1 | - | M | `D` = Daily<br>`W` = Weekly<br>`M` = Monthly<br>`Q` = Quarterly<br>`S` = Semi-annually<br>`A` = Annually<br>`O` = One Time<br>`T` = Template<br>`N` = Not executed yet |
| 4 | `Remind` | Sub-Frequency | Int | 6 | - |  |  |
| 5 | `LastPosted` | Last Executed | Date | 8 | - |  |  |
| 6 | `NextDeu` | Next Execution | Date | 8 | - |  |  |
| 7 | `EntryCount` | Entries Counter | Int | 6 | - | 0 |  |
| 8 | `Volume` | Transaction Amount | Num | 19.6 | - |  |  |
| 9 | `VolCurr` | Total Currency | nVarChar | 3 | - |  |  |
| 10 | `FinancVol` | Total Monetary Val. of Trans. | Num | 19.6 | - |  |  |
| 11 | `Ref1` | Reference 1 | nVarChar | 200 | - |  |  |
| 12 | `Ref2` | Reference 2 | nVarChar | 200 | - |  |  |
| 13 | `TransCode` | Transaction Code | nVarChar | 4 | - |  |  |
| 14 | `Memo` | Details | nVarChar | 254 | - |  |  |
| 15 | `LimitRtrns` | Returns Limit | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 16 | `Returns` | No. of Returns | Int | 6 | - |  |  |
| 17 | `LimitDate` | Date Limit | Date | 8 | - |  |  |
| 18 | `Instance` | Instance | Int | 6 | - | 0 |  |
| 19 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 20 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 21 | `StampTax` | Stamp Tax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 22 | `AutoVat` | Automatic VAT | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 23 | `ManageWTax` | Manage WTax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 24 | `Ref3` | Reference 3 | nVarChar | 100 | - |  |  |
| 25 | `DeferedTax` | Deferred Tax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 26 | `RcrEntry` | Recurring Entry | Int | 11 | - |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | RcurCode, Instance |
| BYDATE | No | NextDeu |
| RCR_ENTRY | No | RcrEntry |
