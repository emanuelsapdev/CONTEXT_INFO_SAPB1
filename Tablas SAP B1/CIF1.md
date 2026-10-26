# CIF1 - Country Specific Information

- **Tabla:** CIF1
- **Descripción:** Country Specific Information
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CIF1.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `FldAbsEnt` | Field ID | Int | 11 | [OCIF](OCIF.md) |  |  |
| 2 | `Country` | Country/Region Code | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 3 | `TransCRY` | Transaction Country/Region | nVarChar | 3 | - | XX |  |
| 4 | `IsMandImp` | Field is mandatory for import | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 5 | `IsMandExp` | Field is mandatory for export | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 6 | `IsReqAllIm` | Field is required for import | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 7 | `IsReqAllEx` | Field is required for export | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | FldAbsEnt, Country, TransCRY |
