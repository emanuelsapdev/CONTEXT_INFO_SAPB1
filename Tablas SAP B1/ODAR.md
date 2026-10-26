# ODAR - Data Archiving

- **Tabla:** ODAR
- **Descripción:** Data Archiving
- **Cantidad de campos:** 33
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ODAR.html

## Campos (33)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Numerator | Int | 11 | - |  |  |
| 2 | `PeriodDate` | Period Date | Date | 8 | - |  |  |
| 3 | `UserSign` | User Signature | Int | 6 | - |  |  |
| 4 | `CreateDate` | Archive Date | Date | 8 | - |  |  |
| 5 | `CreateTime` | Archive Time | Int | 6 | - |  |  |
| 6 | `VersionNum` | Version Number | Int | 11 | - |  |  |
| 7 | `JEPerLen` | Journal Entry Period Length | VarChar | 1 | - | A | `A` = Period<br>`S` = Sub-period<br>`M` = Month |
| 8 | `JERef1` | Journal Entry Reference 1 | nVarChar | 100 | - |  |  |
| 9 | `JERef2` | Journal Entry Reference 2 | nVarChar | 100 | - |  |  |
| 10 | `JEMemo` | Journal Entry Remarks | nVarChar | 254 | - |  |  |
| 11 | `JEByProj` | Journal Entry By Project | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 12 | `JEByProf` | Journal Entry By Dist. Rule | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 13 | `INPerLen` | Inventory Period Length | VarChar | 1 | - | A | `A` = Period<br>`S` = Sub-period<br>`M` = Month |
| 14 | `INPriceSrc` | Inventory Price Source | Int | 6 | [OPLN](OPLN.md) |  |  |
| 15 | `INRef1` | Inventory Reference 1 | nVarChar | 11 | - |  |  |
| 16 | `INRef2` | Inventory Reference 2 | nVarChar | 11 | - |  |  |
| 17 | `INMemo` | Inventory Remarks | nVarChar | 254 | - |  |  |
| 18 | `JEByCurr` | Journal Entry by Currency | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 19 | `JEByDIM2` | Journal Entry by Dimension 2 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 20 | `JEByDIM3` | Journal Entry by Dimension 3 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 21 | `JEByDIM4` | Journal Entry by Dimension 4 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 22 | `JEByDIM5` | Journal Entry by Dimension 5 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 23 | `DBReduc` | DB Reduction (MB) | Num | 19.6 | - |  |  |
| 24 | `DBReducPer` | DB Reduction (%) | Num | 19.6 | - |  |  |
| 25 | `TrandReduc` | Transaction Reduction | Int | 11 | - |  |  |
| 26 | `TranReducP` | Transaction Reduction (%) | Num | 19.6 | - |  |  |
| 27 | `INZeroPrc` | Inventory Zero Price | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 28 | `TranRedArP` | Trans. Reduc. Archived (%) | Num | 19.6 | - |  |  |
| 29 | `DelNonReco` | Delete nonreconciled OBNK lns | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 30 | `RunName` | Data Archive Run Name | nVarChar | 50 | - |  |  |
| 31 | `RODBGUID` | Readonly DB GUID for Archiving | nVarChar | 32 | - |  |  |
| 32 | `ArchMethod` | Archive Method | VarChar | 1 | - | F | `F` = By Financial Period<br>`B` = By Business Partner<br>`R` = Documents |
| 33 | `DocSelect` | Documents Selection | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
