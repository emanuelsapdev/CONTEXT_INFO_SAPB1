# IRD1 - Report Definition - Rows

- **Tabla:** IRD1
- **Descripción:** Report Definition - Rows
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/IRD1.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ReportId` | Report Id | nVarChar | 254 | [OIRD](OIRD.md) |  |  |
| 2 | `Type` | Type | Int | 11 | - | 1 | `1` = XLSX |
| 3 | `Template` | Template | Text | 16 | - |  |  |
| 4 | `CreateBy` | Created By | nVarChar | 25 | - |  |  |
| 5 | `CreateDate` | Creation Timestamp | Date | 8 | - |  |  |
| 6 | `ModifyBy` | Modified By | nVarChar | 25 | - |  |  |
| 7 | `ModifyDate` | Modification Timestamp | Date | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ReportId, Type |
