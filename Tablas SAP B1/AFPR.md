# AFPR - Posting Period-Log

- **Tabla:** AFPR
- **Descripción:** Posting Period-Log
- **Cantidad de campos:** 25
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AFPR.html

## Campos (25)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | System Number | Int | 11 | - |  |  |
| 2 | `Code` | Period Code | nVarChar | 20 | - |  |  |
| 3 | `Name` | Period Name | nVarChar | 20 | - |  |  |
| 4 | `F_RefDate` | Posting Date From | Date | 8 | - |  |  |
| 5 | `T_RefDate` | Posting Date To | Date | 8 | - |  |  |
| 6 | `F_DueDate` | Due Date From | Date | 8 | - |  |  |
| 7 | `T_DueDate` | Due Date To | Date | 8 | - |  |  |
| 8 | `F_TaxDate` | Document Date From | Date | 8 | - |  |  |
| 9 | `T_TaxDate` | Document Date To | Date | 8 | - |  |  |
| 10 | `Free2` | Active for Feed | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 11 | `Free3` | Locked | VarChar | 1 | - | N | `N` = Unlocked<br>`S` = Unlocked Except Sales<br>`C` = Closing Period<br>`Y` = Locked |
| 12 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 13 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 14 | `SubNum` | No. of Sub-Period | Int | 11 | - |  |  |
| 15 | `Free` | Free | VarChar | 1 | - |  |  |
| 16 | `Free1` | Free1 | VarChar | 1 | - |  |  |
| 17 | `Addition` | Additional Sub-Periods | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 18 | `AddNum` | No. of Additional | Int | 11 | - |  |  |
| 19 | `Category` | Category | nVarChar | 10 | [OACP](OACP.md) |  |  |
| 20 | `Indicator` | Period Indicator | nVarChar | 10 | [OPID](OPID.md) |  |  |
| 21 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 22 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 23 | `WasStatChd` | Status Was Checked | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 24 | `PeriodStat` | Period Status | VarChar | 1 | - | N | `N` = Unlocked<br>`S` = Unlocked Except Sales<br>`C` = Closing Period<br>`Y` = Locked<br>`A` = Archived |
| 25 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LogInstanc |
