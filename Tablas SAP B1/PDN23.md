# PDN23 - A/P Invoice - Selected Asset Master Data

- **Tabla:** PDN23
- **Descripción:** A/P Invoice - Selected Asset Master Data
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/PDN23.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | [OPDN](OPDN.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `AssetCode` | Selected Asset Code | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 4 | `Status` | Status | VarChar | 1 | - | O | `O` = Open<br>`C` = Closed |
| 5 | `Remarks` | Remarks | nVarChar | 100 | - |  |  |
| 6 | `Amount` | Amount | Num | 19.6 | - |  |  |
| 7 | `AmountSC` | Amount (SC) | Num | 19.6 | - |  |  |
| 8 | `SerialNo` | Serial Number | nVarChar | 30 | - |  |  |
| 9 | `VisOrder` | Visual Order | Int | 11 | - |  |  |
| 10 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 11 | `ObjectType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 20 |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum, VisOrder |
| ASSETS | No | DocEntry, LineNum, AssetCode |
