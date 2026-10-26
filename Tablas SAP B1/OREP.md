# OREP - Web Client Reports

- **Tabla:** OREP
- **Descripción:** Web Client Reports
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OREP.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Guid` | Report Guid | nVarChar | 32 | - |  |  |
| 2 | `RepName` | Report Name | nVarChar | 120 | - |  |  |
| 3 | `Author` | Report Author | nVarChar | 155 | - |  |  |
| 4 | `Type` | Report Type | nVarChar | 50 | - |  |  |
| 5 | `Category` | Report Category | nVarChar | 120 | - |  |  |
| 6 | `IsSystem` | Is System | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 7 | `Meta` | Report Meta | Text | 16 | - |  |  |
| 8 | `CreateDate` | Create Date | Date | 8 | - |  |  |
| 9 | `UpdateDate` | Update Date | Date | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Guid |
