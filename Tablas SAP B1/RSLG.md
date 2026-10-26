# RSLG - Resource Merge Log

- **Tabla:** RSLG
- **Descripción:** Resource Merge Log
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RSLG.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `SourceDB` | Source DB | Int | 11 | - |  |  |
| 2 | `TargetDB` | Target DB | Int | 11 | - |  |  |
| 3 | `RSName` | Resource Name | nVarChar | 64 | - |  |  |
| 4 | `RSType` | Resource Type | Int | 11 | - |  |  |
| 5 | `RSStatus` | Resourc Status | VarChar | 1 | - | N | `D` = Difference<br>`C` = Conflict<br>`M` = Merged<br>`N` = No Differences |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | SourceDB, TargetDB, RSName, RSType |
