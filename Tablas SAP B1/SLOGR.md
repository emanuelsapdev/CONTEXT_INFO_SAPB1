# SLOGR - SLOGR

- **Tabla:** SLOGR
- **Descripción:** SLOGR
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SLOGR.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `LogKey` | Table key | Identity | 11 | - |  |  |
| 2 | `CompName` | Computer Name | nVarChar | 100 | - |  |  |
| 3 | `LoginName` | Login Name | nVarChar | 100 | - |  |  |
| 4 | `ProcessID` | Process ID | Int | 11 | - |  |  |
| 5 | `LogDate` | Log file date | Date | 8 | - |  |  |
| 6 | `LogFile` | Log file blob | Text | 16 | - |  |  |
| 7 | `Archive` | Archive type | Int | 11 | - | 0 | `1` = AuditArchive<br>`0` = NotArchive |
| 8 | `CrashTime` | Time of the crash | nVarChar | 14 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | LogKey |
