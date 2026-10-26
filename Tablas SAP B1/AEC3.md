# AEC3 - Statuses and Logs for Actions in Electronic Communication

- **Tabla:** AEC3
- **Descripción:** Statuses and Logs for Actions in Electronic Communication
- **Cantidad de campos:** 18
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AEC3.html

## Campos (18)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal ID | Int | 11 | [ECM2](ECM2.md) |  |  |
| 2 | `LogNum` | Log Number | Int | 11 | - |  |  |
| 3 | `LogType` | Log Type | VarChar | 1 | - | R | `S` = Send<br>`R` = Receive<br>`I` = Import<br>`N` = Note<br>`W` = Warning<br>`E` = Error<br>`D` = WS Data<br>`B` = Authorities Process Starts<br>`F` = Authorities Process Finished |
| 4 | `LogMessage` | Log Message | Text | 16 | - |  |  |
| 5 | `LogData` | Log Data | Text | 16 | - |  |  |
| 6 | `LogOpDate` | Log Operation Date | Date | 8 | - |  |  |
| 7 | `LogOpTS` | Log Operation Time - Incl. Secs | Int | 11 | - |  |  |
| 8 | `ExportFmt` | Export Format | Int | 11 | [OLLF](OLLF.md) |  |  |
| 9 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 10 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 11 | `CreateTS` | Create Time - Incl. Secs | Int | 11 | - |  |  |
| 12 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 13 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 14 | `UpdateTS` | Update Time - Incl. Secs | Int | 11 | - |  |  |
| 15 | `LogInstanc` | Log Instance | Int | 6 | - |  |  |
| 16 | `ExportFile` | Export File | Text | 16 | - |  |  |
| 17 | `AutProcess` | Authorities Process | VarChar | 1 | - |  | None<br>`A` = Approval Process<br>`R` = Rejection Process |
| 18 | `Sensitive` | Log is Sensitive | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LogNum, LogInstanc |
