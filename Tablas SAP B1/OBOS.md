# OBOS - Box Set Definition

- **Tabla:** OBOS
- **Descripción:** Box Set Definition
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OBOS.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `IsUsed` | Is Set Used | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 3 | `EffecDate` | Effective From | Date | 8 | - |  |  |
| 4 | `FileFmtCo` | File Format Code | Int | 11 | [OLLF](OLLF.md) |  |  |
| 5 | `IsDeleted` | Is Set Deleted | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `ReportType` | Report Type | VarChar | 1 | - | S | `B` = Box Declaration<br>`S` = BAS Report |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| EFFEC_DATE | No | EffecDate |
| BZKEY | No | EffecDate, ReportType |
