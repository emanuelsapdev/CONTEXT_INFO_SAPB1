# SLSC - Local Settings Components CABs

- **Tabla:** SLSC
- **Descripción:** Local Settings Components CABs
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SLSC.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `LocCode` | LocalCode | nVarChar | 3 | - |  |  |
| 2 | `Code` | Code | nVarChar | 20 | - |  |  |
| 3 | `Name` | Name | nVarChar | 100 | - |  |  |
| 4 | `Type` | Type | VarChar | 1 | - |  | `C` = Chart of accounts<br>`R` = Reports<br>`O` = Objects<br>`P` = CR Report<br>`L` = CR Layout<br>`H` = HANA Content |
| 5 | `DataCab` | Data CAB | Text | 16 | - |  |  |
| 6 | `System` | System package | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | LocCode, Code |
