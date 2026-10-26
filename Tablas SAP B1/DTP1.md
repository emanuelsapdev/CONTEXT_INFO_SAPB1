# DTP1 - Depreciation Types - Rows

- **Tabla:** DTP1
- **Descripción:** Depreciation Types - Rows
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/DTP1.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Code | nVarChar | 15 | [ODTP](ODTP.md) |  |  |
| 2 | `Level` | Level | Int | 11 | - |  |  |
| 3 | `Base` | Base | nVarChar | 3 | - | APC | `APC` = Acquisition Value<br>`NBV` = Net Book Value |
| 4 | `Years` | Number of Years | Int | 11 | - |  |  |
| 5 | `Percentage` | Percentage | Num | 19.6 | - |  |  |
| 6 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 7 | `Amount` | Amount | Num | 19.6 | - |  |  |
| 8 | `SnapshotId` | Snapshot ID | Int | 11 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code, Level |
