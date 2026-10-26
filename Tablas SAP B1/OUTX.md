# OUTX - Unreported VAT Transactions

- **Tabla:** OUTX
- **Descripción:** Unreported VAT Transactions
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OUTX.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `SrcObjType` | Source Object Type | nVarChar | 20 | - | -1 | `-1`<br>`15` = Delivery notes<br>`16` = Revert Delivery Notes<br>`17` = Sales Order<br>`20` = Goods Receipt<br>`21` = Goods Return<br>`22` = Purchase order<br>`23` = Sales Quotation<br>`112` = Document Draft<br>`59` = Goods Receipt<br>`60` = Goods Issue<br>`28` = Journal Batches<br>`140` = Payment Draft<br>`123` = Checks for Payment Drafts<br>`540000006` = Purchase Quotation |
| 3 | `SrcObjAbs` | Source Object Internal ID | Int | 11 | - | -1 |  |
| 4 | `OrdinLNum` | Ordial Num (BTF & Canceled) | Int | 11 | - | -1 |  |
| 5 | `Cancelled` | Canceled | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| SECONDARY | Yes | SrcObjType, SrcObjAbs, OrdinLNum |
