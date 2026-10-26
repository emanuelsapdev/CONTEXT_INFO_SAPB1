# OIRD - Report Definition

- **Tabla:** OIRD
- **Descripción:** Report Definition
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OIRD.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ReportId` | Report Id | nVarChar | 254 | - |  |  |
| 2 | `Type` | Type | Int | 11 | - | 1 |  |
| 3 | `CategoryId` | Category Id | Int | 11 | - |  |  |
| 4 | `Revision` | Revision | nVarChar | 10 | - |  |  |
| 5 | `Title` | Title | nVarChar | 254 | - |  |  |
| 6 | `Definition` | Report Definition | Text | 16 | - |  |  |
| 7 | `System` | System | VarChar | 1 | - |  |  |
| 8 | `CreateBy` | Created By | nVarChar | 25 | - |  |  |
| 9 | `CreateDate` | Creation Timestamp | Date | 8 | - |  |  |
| 10 | `ModifyBy` | Modified By | nVarChar | 25 | - |  |  |
| 11 | `ModifyDate` | Modification Timestamp | Date | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ReportId |
