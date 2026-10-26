# TSI1 - Sales Tax Invoice - Rows1

- **Tabla:** TSI1
- **Descripción:** Sales Tax Invoice - Rows1
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TSI1.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `BaseEntry` | Base Document Internal ID | Int | 11 | [OTSI](OTSI.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `Canceled` | Canceled | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 4 | `DocType` | Document Type | VarChar | 1 | - | I | `I` = Invoice<br>`P` = Payment<br>`J` = Journal Entry<br>`C` = Correction Invoice<br>`L` = Landed Cost |
| 5 | `RefEntry1` | Ref.1 Document Key | Int | 11 | - |  |  |
| 6 | `RefEntry2` | Ref.1 Document Key | Int | 11 | - |  |  |
| 7 | `ObjType` | Object Type | Int | 6 | [ADP1](ADP1.md) |  |  |
| 8 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 9 | `RefType` | Ref. Object Type | Int | 11 | - | -1 | `-1`<br>`13` = A/R Invoice<br>`18` = A/P Invoice<br>`30` = Journal Entry<br>`24` = Incoming Payment<br>`204` = A/P Down Payment<br>`165` = A/R Correction Invoice<br>`163` = A/P Correction Invoice<br>`69` = Landed Cost |
| 10 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | BaseEntry, LineNum |
