# RSAT - RecordSet Audit Table

- **Tabla:** RSAT
- **Descripción:** RecordSet Audit Table
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RSAT.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `QueryID` | Query ID | Identity | 11 | - |  |  |
| 2 | `QueryDate` | Date of Query | Int | 11 | - |  |  |
| 3 | `QueryTime` | Timestamp of Query | Int | 11 | - |  |  |
| 4 | `QueryDetls` | Query Details | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | QueryID |
