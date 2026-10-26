# PDF8 - Payment Draft - TDS Entries

- **Tabla:** PDF8
- **Descripción:** Payment Draft - TDS Entries
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/PDF8.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocNum` | Document Number | Int | 11 | [OPDF](OPDF.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `InvType` | Invoice Category | nVarChar | 20 | - | -1 | `-1` = All Transactions<br>`204` = A/P Down Payment<br>`18` = A/P Invoice<br>`19` = A/P Credit Memo<br>`10000079` = TDS Adjustment |
| 4 | `DocEntry` | Invoice Internal ID | Int | 11 | - |  |  |
| 5 | `DocLine` | Invoice Row Number | Int | 11 | - |  |  |
| 6 | `ObjectType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) |  |  |
| 7 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 8 | `PaidEntry` | Payment Internal ID | Int | 11 | - |  |  |
| 9 | `PaidLine` | Payment Row Number | Int | 11 | - |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocNum, LineNum |
| INVOICE | No | InvType, DocEntry, DocLine |
| PAYMENT | No | PaidEntry, PaidLine |
