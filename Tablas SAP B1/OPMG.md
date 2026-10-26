# OPMG - Project Management Document

- **Tabla:** OPMG
- **Descripción:** Project Management Document
- **Cantidad de campos:** 33
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OPMG.html

## Campos (33)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | - |  |  |
| 2 | `OWNER` | Owner | Int | 11 | [OHEM](OHEM.md) |  |  |
| 3 | `NAME` | Project Name | nVarChar | 254 | - |  |  |
| 4 | `START` | Project Start Date | Date | 8 | - |  |  |
| 5 | `FINISHED` | Deduction - Percentage | Num | 19.6 | - |  |  |
| 6 | `DocNum` | Document Number | Int | 11 | - |  |  |
| 7 | `Series` | Series | Int | 11 | - |  |  |
| 8 | `TYP` | Project Type | VarChar | 1 | - | E | `E` = External<br>`I` = Internal |
| 9 | `CARDCODE` | BP Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 10 | `CARDNAME` | BP Name | nVarChar | 200 | - |  |  |
| 11 | `CONTACT` | Contact Person | Int | 11 | [OCPR](OCPR.md) |  |  |
| 12 | `TERRITORY` | Business Partner Territory | Int | 11 | [OTER](OTER.md) |  |  |
| 13 | `EMPLOYEE` | Sales Employee | Int | 11 | [OSLP](OSLP.md) | -1 |  |
| 14 | `WithPhases` | Project with Phases | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 15 | `STATUS` | Status | VarChar | 1 | - | S | `S` = Started<br>`P` = Paused<br>`T` = Stopped<br>`F` = Finished<br>`N` = Canceled |
| 16 | `DUEDATE` | Due Date | Date | 8 | - |  |  |
| 17 | `CLOSING` | Closing Date | Date | 8 | - |  |  |
| 18 | `FIPROJECT` | Financial Project | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 19 | `RISK` | Risk Level | VarChar | 1 | - | L | `L` = Low<br>`M` = Medium<br>`H` = High |
| 20 | `INDUSTRY` | Industry Code | Int | 11 | [OOND](OOND.md) |  |  |
| 21 | `REASON` | Comments | Text | 16 | - |  |  |
| 22 | `Free_Text` | Free Text | Text | 16 | - |  |  |
| 23 | `BPLid` | Business Place ID | Int | 11 | [OBPL](OBPL.md) |  |  |
| 24 | `AtcEntry` | Attachment Entry | Int | 11 | [OATC](OATC.md) |  |  |
| 25 | `Attachment` | Attachments | Text | 16 | - |  |  |
| 26 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 27 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 28 | `UserSign` | User Signature | Int | 6 | - |  |  |
| 29 | `UserSign2` | Updating User | Int | 6 | - |  |  |
| 30 | `CreateDate` | Production Date | Date | 8 | - |  |  |
| 31 | `UpdateTS` | Update Full Time | Int | 11 | - |  |  |
| 32 | `DPPStatus` | Data Protection Status | VarChar | 1 | - | N | `N` = None<br>`D` = Erased |
| 33 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
