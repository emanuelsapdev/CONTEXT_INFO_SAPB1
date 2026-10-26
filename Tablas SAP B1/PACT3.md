# PACT3 - Pervasive's Insight to Action's Table Field

- **Tabla:** PACT3
- **Descripción:** Pervasive's Insight to Action's Table Field
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/PACT3.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `ActItemEnt` | Action Item Number | Int | 11 | - |  |  |
| 3 | `TableName` | Table Name | nVarChar | 50 | - |  |  |
| 4 | `FieldName` | Field Name | nVarChar | 50 | - |  |  |
| 5 | `IsUDF` | Is UDF or Not | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
