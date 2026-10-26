# ITM10 - OITM Extension

- **Tabla:** ITM10
- **Descripción:** OITM Extension
- **Cantidad de campos:** 20
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ITM10.html

## Campos (20)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 2 | `ISCommCode` | Commodity Code | Int | 11 | [ODCI](ODCI.md) |  |  |
| 3 | `ISSubMasUn` | Intrastat Additional Measure | Int | 11 | [ODCI](ODCI.md) |  |  |
| 4 | `ISFactor` | IS Factor Additional Measure | Num | 19.6 | - |  |  |
| 5 | `ISOrCSTImp` | IS Destination State for Impor. | Int | 11 | [ODCI](ODCI.md) |  |  |
| 6 | `ISOrCSTExp` | IS State of Origin for Export | Int | 11 | [ODCI](ODCI.md) |  |  |
| 7 | `ISNaTraImp` | IS Nature of Trans. Import | Int | 11 | [ODCI](ODCI.md) |  |  |
| 8 | `ISNaTraExp` | IS Nature of Trans. Export | Int | 11 | [ODCI](ODCI.md) |  |  |
| 9 | `ISStProImp` | IS Statistical Procedure Imp. | Int | 11 | [ODCI](ODCI.md) |  |  |
| 10 | `ISStProExp` | IS Statistical Procedure Exp. | Int | 11 | [ODCI](ODCI.md) |  |  |
| 11 | `ISOriCntry` | Intrastat Country of Origin | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 12 | `ISSerCode` | Intrastat Service Code | Int | 11 | [ODCI](ODCI.md) |  |  |
| 13 | `ISItemType` | Intrastat Item Type | VarChar | 1 | - | I | `I` = Item<br>`S` = Service |
| 14 | `ISSerSupMt` | IS Service Supply Method | nVarChar | 12 | - | I | `I` = Immediate<br>`R` = To More Resumptions |
| 15 | `ISSerPayMt` | IS Service Payment Method | nVarChar | 12 | - | X | `A` = Accredited to Bank Account<br>`B` = Bank Transfer<br>`X` = Other |
| 16 | `ISOrCRYImp` | IS Destination Country for Imp. | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 17 | `ISOrCRYExp` | IS Origin Country for Export | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 18 | `ISUseWeigh` | Use Wt in Add. Measure Calc. | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 19 | `ISRelevant` | Intrastat Relevant | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 20 | `ISStatCode` | Statistical Code | nVarChar | 2 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ItemCode |
