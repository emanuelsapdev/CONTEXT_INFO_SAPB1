# ASH1 - Time Sheet - Rows - History

- **Tabla:** ASH1
- **Descripción:** Time Sheet - Rows - History
- **Cantidad de campos:** 32
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ASH1.html

## Campos (32)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | - |  |  |
| 2 | `LineID` | Row No. | Int | 11 | - |  |  |
| 3 | `Date` | Date | Date | 8 | - |  |  |
| 4 | `ActType` | Activity Type | Int | 11 | [PMC5](PMC5.md) |  |  |
| 5 | `LaborItem` | Labor Item No. | nVarChar | 50 | - |  |  |
| 6 | `StartTime` | Start Time | Int | 11 | - |  |  |
| 7 | `EndTime` | End Time | Int | 11 | - |  |  |
| 8 | `Workorder` | Workorder Doc. Entry | Int | 11 | [OWOR](OWOR.md) |  |  |
| 9 | `WorAbs` | Workorder Abs. Entry | Int | 11 | - |  |  |
| 10 | `ServCall` | Service Call ID | Int | 11 | [OSCL](OSCL.md) |  |  |
| 11 | `CostCenter` | Cost Center | nVarChar | 8 | - |  |  |
| 12 | `FiProject` | Financial Project | nVarChar | 20 | - |  |  |
| 13 | `Location` | Location | Int | 11 | - |  |  |
| 14 | `GPSData` | GPS Data | nVarChar | 50 | - |  |  |
| 15 | `Branch` | Branch ID | Int | 11 | [OBPL](OBPL.md) |  |  |
| 16 | `Break` | Break | Int | 11 | - |  |  |
| 17 | `NonBillTm` | Nonbillable Time | Int | 11 | - |  |  |
| 18 | `EffectTm` | Effective Time | Int | 11 | - |  |  |
| 19 | `BillableTm` | Billable Time | Int | 11 | - |  |  |
| 20 | `FullDay` | Full Day | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 21 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 22 | `ProjectID` | Project or Subproject ID | Int | 11 | - |  |  |
| 23 | `Subproject` | Subproject ID | Int | 11 | - |  |  |
| 24 | `StageID` | Stage ID | Int | 11 | - |  |  |
| 25 | `Charged` | Charged | Num | 19.6 | - |  |  |
| 26 | `Chargeable` | Chargeable [Yes/No] | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 27 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 28 | `BreakHr` | Break Hours | Num | 19.6 | - |  |  |
| 29 | `NonBillHr` | Non-Billable Hours | Num | 19.6 | - |  |  |
| 30 | `EffectHr` | Effective Hours | Num | 19.6 | - |  |  |
| 31 | `BillableHr` | Billable Hours | Num | 19.6 | - |  |  |
| 32 | `EnActType` | Encrypt Activity Type | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineID, LogInstanc |
