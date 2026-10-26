# BOX3 - Box Definition - Choice

- **Tabla:** BOX3
- **Descripción:** Box Definition - Choice
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/BOX3.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `BoxCode` | Group Code | nVarChar | 30 | - |  |  |
| 2 | `ReportType` | Report Type | VarChar | 1 | - | B | `B`<br>`S` |
| 3 | `Value` | Value | nVarChar | 8 | - |  |  |
| 4 | `Descr` | Description | nVarChar | 250 | - |  |  |
| 5 | `EffecDate` | Effective From | Date | 8 | - |  |  |
| 6 | `BosCode` | Box Set Code | Int | 11 | [OBOS](OBOS.md) |  |  |
| 7 | `IsDefault` | Is Default | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | BoxCode, ReportType, BosCode, Value |
