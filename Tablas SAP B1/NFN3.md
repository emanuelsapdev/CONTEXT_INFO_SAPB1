# NFN3 - Assigned Nota Fiscal Series

- **Tabla:** NFN3
- **Descripción:** Assigned Nota Fiscal Series
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/NFN3.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ObjectCode` | Document | nVarChar | 20 | [ONFN](ONFN.md) |  |  |
| 2 | `SeqCode` | Sequence Code | Int | 6 | - | 0 |  |
| 3 | `DocSubType` | VAT Code for Tax Invoice Rpt | nVarChar | 2 | - | -- |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ObjectCode, DocSubType, SeqCode |
| SEQ | No | SeqCode |
