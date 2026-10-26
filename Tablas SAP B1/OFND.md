# OFND - Folio Numbering Documents

- **Tabla:** OFND
- **Descripción:** Folio Numbering Documents
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OFND.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `ObjectCode` | Document | nVarChar | 20 | - |  |  |
| 3 | `DocSubtype` | Subdocument | nVarChar | 2 | - | -- | `--`<br>`DM` = A/P Debit Memo<br>`DN` = A/R Debit Memo<br>`IB` = A/R Bill |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| OBJECT | Yes | ObjectCode, DocSubtype |
