# MIV1 - A/P Monthly Invoice - Document

- **Tabla:** MIV1
- **Descripción:** A/P Monthly Invoice - Document
- **Cantidad de campos:** 16
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MIV1.html

## Campos (16)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `MinvNum` | Monthly Invoice Number | Int | 11 | - |  |  |
| 2 | `AbsEntry` | Internal Key | Int | 11 | - |  |  |
| 3 | `DocNum` | Document Number | Int | 11 | - |  |  |
| 4 | `DocType` | Document Object ID | nVarChar | 20 | - |  | `18` = A/P Invoice<br>`19` = A/P Credit Memo |
| 5 | `DocDate` | Document Posting Date | Date | 8 | - |  |  |
| 6 | `DocDueDate` | Document Due Date | Date | 8 | - |  |  |
| 7 | `DocClsDate` | Document Closing Date | Date | 8 | - |  |  |
| 8 | `DocAmount` | Total Amount | Num | 19.6 | - |  |  |
| 9 | `DocExpense` | Document Expense | Num | 19.6 | - |  |  |
| 10 | `DocDiscSum` | Document Discount Sum | Num | 19.6 | - |  |  |
| 11 | `DocRound` | Document Rounding | Num | 19.6 | - |  |  |
| 12 | `DocTax` | Document Tax Amount | Num | 19.6 | - |  |  |
| 13 | `Closed` | Is Document closed in MI | VarChar | 1 | - | N | `Y` = Closed<br>`N` = Not Closed |
| 14 | `MINumWnCls` | absEntry when doc closed | Int | 11 | - |  |  |
| 15 | `Entry` | Monthly Invoice Entry | Int | 11 | [OMIV](OMIV.md) |  |  |
| 16 | `DocOrigin` | Document Origin | VarChar | 1 | - | M | `M` = Manual<br>`A` = Automatic |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Entry, DocType, AbsEntry |
