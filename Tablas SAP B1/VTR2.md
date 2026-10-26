# VTR2 - Doc. Type Filter

- **Tabla:** VTR2
- **Descripción:** Doc. Type Filter
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/VTR2.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `ObjectCode` | Object Code | nVarChar | 15 | - |  | `13` = A/R Invoices<br>`14` = A/R Credit Memos<br>`18` = A/P Invoices<br>`19` = A/P Credit Memos<br>`24` = Incoming Payments<br>`30` = Journal Entries<br>`46` = Outgoing Payments<br>`57` = Checks for Payment<br>`67` = Inventory Transfers<br>`203` = A/R Down Payment<br>`204` = A/P Down Payment |
| 3 | `FromDocNo` | Doc. Number From | Int | 11 | - |  |  |
| 4 | `ToDocNo` | To Doc Number | Int | 11 | - |  |  |
| 5 | `Selected` | Is Selected Object. | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, ObjectCode |
