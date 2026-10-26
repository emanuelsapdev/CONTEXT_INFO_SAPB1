# OLLR - Electronic Report Generation Result

- **Tabla:** OLLR
- **Descripción:** Electronic Report Generation Result
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OLLR.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 3 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 4 | `CreateTime` | Creation Time | Int | 6 | - |  |  |
| 5 | `EReportId` | Electronic Report ID | Int | 11 | [OLLF](OLLF.md) |  |  |
| 6 | `Status` | Status | VarChar | 1 | - | C | `C` = Canceled<br>`E` = Executed<br>`F` = Failed |
| 7 | `Log` | Run Log | Text | 16 | - |  |  |
| 8 | `ReportInst` | Electronic Report Instance | Int | 11 | - |  |  |
| 9 | `VersionNum` | Version Number | nVarChar | 13 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| REPORT | No | EReportId |
