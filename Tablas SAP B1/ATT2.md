# ATT2 - BOM - Route Stages - History

- **Tabla:** ATT2
- **Descripción:** BOM - Route Stages - History
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ATT2.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Father` | Parent Item | nVarChar | 50 | [OITT](OITT.md) |  |  |
| 2 | `StageId` | Stage ID | Int | 11 | - |  |  |
| 3 | `SeqNum` | Sequence Number | Int | 11 | - |  |  |
| 4 | `StgEntry` | Stage Entry | Int | 11 | [ORST](ORST.md) |  |  |
| 5 | `Name` | Stage Name | nVarChar | 100 | - |  |  |
| 6 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 7 | `WaitDays` | Waiting Days | Num | 19.6 | - | 0 |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Father, StageId, LogInstanc |
| SEQUENCE | Yes | Father, SeqNum, LogInstanc |
