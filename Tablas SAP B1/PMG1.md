# PMG1 - Project Management - Stages

- **Tabla:** PMG1
- **Descripción:** Project Management - Stages
- **Cantidad de campos:** 33
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/PMG1.html

## Campos (33)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | [OPMG](OPMG.md) |  |  |
| 2 | `LineID` | Row No. | Int | 11 | - |  |  |
| 3 | `StageID` | Stage ID | Int | 11 | [PMC2](PMC2.md) |  |  |
| 4 | `POS` | Position | Int | 11 | - |  |  |
| 5 | `START` | Start Date | Date | 8 | - |  |  |
| 6 | `CLOSE` | Closing Date | Date | 8 | - |  |  |
| 7 | `FINISHDATE` | Finished Date | Date | 8 | - |  |  |
| 8 | `Task` | Task Type | Int | 11 | - |  |  |
| 9 | `DSCRIPTION` | Description | Text | 16 | - |  |  |
| 10 | `EXPCOSTS` | Planned Cost | Num | 19.6 | - |  |  |
| 11 | `InvAmtAR` | Invoiced Amount (A/R) | Num | 19.6 | - |  |  |
| 12 | `OpenAmtAR` | Open Amount (A/R) | Num | 19.6 | - |  |  |
| 13 | `InvAmtAP` | Invoiced Amount (A/P) | Num | 19.6 | - |  |  |
| 14 | `OpenAmtAP` | Open Amount (A/P) | Num | 19.6 | - |  |  |
| 15 | `PERCENT` | Contribution Rate - Percentage | Num | 19.6 | - |  |  |
| 16 | `FINISH` | Finished | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 17 | `OWNER` | Owner | Int | 11 | [OHEM](OHEM.md) |  |  |
| 18 | `StageDep1` | Stage Dependence (1) | Int | 11 | - |  |  |
| 19 | `StageDep2` | Stage Dependence (2) | Int | 11 | - |  |  |
| 20 | `StageDep3` | Stage Dependence (3) | Int | 11 | - |  |  |
| 21 | `StageDep4` | Stage Dependence (4) | Int | 11 | - |  |  |
| 22 | `StDp1Type` | Stage Dependence (1) project type | VarChar | 1 | - | P | `P` = Project<br>`S` = Subproject |
| 23 | `StDp2Type` | Stage Dependence (2) project type | VarChar | 1 | - | P | `P` = Project<br>`S` = Subproject |
| 24 | `StDp3Type` | Stage Dependence (3) project type | VarChar | 1 | - | P | `P` = Project<br>`S` = Subproject |
| 25 | `StDp4Type` | Stage Dependence (4) project type | VarChar | 1 | - | P | `P` = Project<br>`S` = Subproject |
| 26 | `StDp1Abs` | Stage Dependence (1) project key | Int | 11 | - |  |  |
| 27 | `StDp2Abs` | Stage Dependence (2) project key | Int | 11 | - |  |  |
| 28 | `StDp3Abs` | Stage Dependence (3) project key | Int | 11 | - |  |  |
| 29 | `StDp4Abs` | Stage Dependence (4) project key | Int | 11 | - |  |  |
| 30 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 31 | `AtcEntry` | Attachment Entry | Int | 11 | [OATC](OATC.md) |  |  |
| 32 | `UniqueID` | Unique ID | nVarChar | 50 | - |  |  |
| 33 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineID |
| POS | Yes | AbsEntry, POS |
