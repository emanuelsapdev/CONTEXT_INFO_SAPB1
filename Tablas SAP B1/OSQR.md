# OSQR - Standard Queries

- **Tabla:** OSQR
- **Descripción:** Standard Queries
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSQR.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `IntrnalKey` | Internal Key | Int | 11 | - |  |  |
| 2 | `QCategory` | Query Group | Int | 11 | - |  |  |
| 3 | `QName` | Query Name | nVarChar | 100 | - |  |  |
| 4 | `QString` | Query | Text | 16 | - |  |  |
| 5 | `QType` | Query Type | VarChar | 1 | - | R | `R` = Regular<br>`W` = Wizard<br>`G` = Report Generator |
| 6 | `ColumnSize` | Column Size | nVarChar | 100 | - |  |  |
| 7 | `DBType` | DB Type | Int | 11 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | IntrnalKey |
| QNAME_K | Yes | QName |
