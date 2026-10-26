# ODAB - Dashboard

- **Tabla:** ODAB
- **Descripción:** Dashboard
- **Cantidad de campos:** 14
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ODAB.html

## Campos (14)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | - |  |  |
| 2 | `PackEntry` | Package Entry | Int | 11 | [OWPK](OWPK.md) |  |  |
| 3 | `DashbdCode` | Dashboard Code | nVarChar | 32 | - |  |  |
| 4 | `DashbdName` | Dashboard Name | nVarChar | 100 | - |  |  |
| 5 | `DashbdPath` | Dashboard Path | nVarChar | 254 | - |  |  |
| 6 | `Note` | Dashboard Description | Text | 16 | - |  |  |
| 7 | `Status` | Dashboard Status | VarChar | 1 | - | A | `I` = Inactive<br>`A` = Active |
| 8 | `JobFlag` | Use Schedule Job Flag | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 9 | `JobType` | Schedule Job Type | VarChar | 1 | - | R | `R` = Real Time<br>`P` = Periodic |
| 10 | `JobSetting` | Schedule Job Time Setting | nVarChar | 100 | - |  |  |
| 11 | `RenewDate` | Latest Renew Date | Date | 8 | - |  |  |
| 12 | `RenewTime` | Latest Renew Time | Int | 6 | - |  |  |
| 13 | `ProcName` | Procedure Name | nVarChar | 100 | - |  |  |
| 14 | `JobName` | Schedule Job Name | nVarChar | 100 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| CODE | Yes | PackEntry, DashbdCode |
