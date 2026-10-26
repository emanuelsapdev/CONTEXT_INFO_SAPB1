# PDF7 - Payment Draft - Tax Amount per Document

- **Tabla:** PDF7
- **Descripción:** Payment Draft - Tax Amount per Document
- **Cantidad de campos:** 14
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/PDF7.html

## Campos (14)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocNum` | Document Number | Int | 11 | [OPDF](OPDF.md) |  |  |
| 2 | `LineSeq` | Row Sequence | Int | 11 | - |  |  |
| 3 | `InvoiceSeq` | Invoice Sequence Number | Int | 11 | - |  |  |
| 4 | `ValueDate` | Due Date | Date | 8 | - |  |  |
| 5 | `Inv4Seq` | INV4 Sequence Number | Int | 11 | - |  |  |
| 6 | `TaxSum` | Tax Amount | Num | 19.6 | - |  |  |
| 7 | `TaxSumFrgn` | Tax Amount (FC) | Num | 19.6 | - |  |  |
| 8 | `TaxSumSys` | Tax Amount (SC) | Num | 19.6 | - |  |  |
| 9 | `BaseSum` | Base Amount | Num | 19.6 | - |  |  |
| 10 | `BaseSumFrg` | Base Amount (FC) | Num | 19.6 | - |  |  |
| 11 | `BaseSumSys` | Base Amount (SC) | Num | 19.6 | - |  |  |
| 12 | `ObjectType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 24 |  |
| 13 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 14 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocNum, LineSeq |
