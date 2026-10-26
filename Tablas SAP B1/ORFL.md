# ORFL - Already Displayed 347, 349 and WTax Reports

- **Tabla:** ORFL
- **Descripción:** Already Displayed 347, 349 and WTax Reports
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ORFL.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ReportType` | Report Type | Int | 11 | - |  | `1` = 347<br>`2` = 349<br>`3` = WT<br>`4` = O & P<br>`5` = Annual List<br>`6` = Tax Report |
| 2 | `DocType` | Document Type | nVarChar | 20 | - |  | `13` = Invoice<br>`14` = Revert Invoice<br>`18` = Purchase<br>`19` = Revert purchase<br>`203` = A/R Down Payment<br>`204` = A/P Down Payment |
| 3 | `DocEntry` | Document Internal ID | Int | 11 | - |  |  |
| 4 | `LineNum` | Row No. | Int | 11 | - |  |  |
| 5 | `TaxCode` | Tax Code | nVarChar | 8 | - |  |  |
| 6 | `OrdinalNum` | Ordinal Num (BTF & Cancelled) | Int | 11 | - | -1 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, ReportType, DocType, LineNum, TaxCode, OrdinalNum |
