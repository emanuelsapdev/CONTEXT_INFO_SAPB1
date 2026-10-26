# ORLD - Reference Links Definition

- **Tabla:** ORLD
- **Descripción:** Reference Links Definition
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ORLD.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `ObjectCode` | Document | nVarChar | 20 | - |  |  |
| 3 | `DocSubType` | Document Subtype | nVarChar | 2 | - | -- | `--`<br>`IE` = Invoice Exempt<br>`DN` = Debit Memo<br>`IB` = Bill<br>`EB` = Exempt Bill<br>`DM` = A/P Debit Memo<br>`IX` = Export Invoice<br>`GA` = GST Tax Invoice<br>`GD` = GST Debit Memo |
| 4 | `Status` | Status | VarChar | 1 | - | O | `O` = Original<br>`C` = Customized |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| OBJ_FIELD | Yes | ObjectCode, DocSubType |
