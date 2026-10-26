# AAC1 - Asset Classes - Depreciation Areas - History

- **Tabla:** AAC1
- **Descripción:** Asset Classes - Depreciation Areas - History
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AAC1.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Code | nVarChar | 20 | [OACS](OACS.md) |  |  |
| 2 | `LineNum` | Line Number | Int | 11 | - |  |  |
| 3 | `DprAreaID` | Depreciation Area ID | nVarChar | 15 | [ODPA](ODPA.md) |  |  |
| 4 | `Active` | Active | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 5 | `AcctDtn` | Account Determination | nVarChar | 15 | [OADT](OADT.md) |  |  |
| 6 | `DprTypID` | Depreciation Type ID | nVarChar | 15 | [ODTP](ODTP.md) |  |  |
| 7 | `UseLife` | Useful Life | Int | 11 | - |  |  |
| 8 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 9 | `SnapshotId` | Snapshot ID | Int | 11 | - | 0 |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code, LineNum, LogInstanc |
| UNIQUE | Yes | Code, DprAreaID, LogInstanc |
