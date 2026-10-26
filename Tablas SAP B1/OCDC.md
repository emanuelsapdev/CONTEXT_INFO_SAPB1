# OCDC - Cash Discount

- **Tabla:** OCDC
- **Descripción:** Cash Discount
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCDC.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Cash Discount Code | nVarChar | 20 | - |  |  |
| 2 | `TableDesc` | Cash Discount Name | nVarChar | 100 | - |  |  |
| 3 | `ByDate` | By Date | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 4 | `Freight` | Freight | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 5 | `Tax` | Tax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `VatCrctn` | VAT Correction | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 7 | `BaseDate` | Base Date | VarChar | 1 | - | P | `P` = Posting Date<br>`S` = System Date<br>`T` = Document Date<br>`C` = Closing Date |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code |
