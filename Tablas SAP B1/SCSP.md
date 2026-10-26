# SCSP - Stored Procs (Company)

- **Tabla:** SCSP
- **Descripción:** Stored Procs (Company)
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SCSP.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `SpName` | SP Name | nVarChar | 50 | - |  |  |
| 2 | `SpString` | SP String | Text | 16 | - |  |  |
| 3 | `doBefore` | Do before | VarChar | 1 | - |  | `Y`<br>`N` |
| 4 | `ForceCreat` | Force Create | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 5 | `ServerType` | Server Type | Int | 11 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | SpName, ServerType |
