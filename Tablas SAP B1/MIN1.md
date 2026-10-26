# MIN1 - Monthly Invoice Report Document Information

- **Tabla:** MIN1
- **Descripción:** Monthly Invoice Report Document Information
- **Cantidad de campos:** 16
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MIN1.html

## Campos (16)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `MinvNum` | Monthly Invoice Number | Int | 11 | - |  |  |
| 2 | `AbsEntry` | Document Internal ID | Int | 11 | - |  |  |
| 3 | `DocNum` | Document Number | Int | 11 | - |  |  |
| 4 | `DocType` | Document Object ID | nVarChar | 20 | - |  | `13` = A/R Invoice<br>`14` = A/R Credit Memo |
| 5 | `DocDate` | Document Posting Date | Date | 8 | - |  |  |
| 6 | `DocDueDate` | Document Due Date | Date | 8 | - |  |  |
| 7 | `DocClsDate` | Document Closing Date | Date | 8 | - |  |  |
| 8 | `DocAmount` | Total Amount | Num | 19.6 | - |  |  |
| 9 | `DocExpense` | Document Expense | Num | 19.6 | - |  |  |
| 10 | `DocDiscSum` | Document Discount Sum | Num | 19.6 | - |  |  |
| 11 | `DocRound` | Document Rounding | Num | 19.6 | - |  |  |
| 12 | `DocTax` | Document Tax Amount | Num | 19.6 | - |  |  |
| 13 | `Closed` | Document Closed? | VarChar | 1 | - | N | `Y`<br>`N` |
| 14 | `MINumWnCls` | Internal Number for Closed Document | Int | 11 | - |  |  |
| 15 | `Entry` | Monthly Invoice Entry | Int | 11 | [OMIN](OMIN.md) |  |  |
| 16 | `DocOrigin` | Document Origin | VarChar | 1 | - | M | `M` = Manual<br>`A` = Automatic |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Entry, DocType, AbsEntry |
