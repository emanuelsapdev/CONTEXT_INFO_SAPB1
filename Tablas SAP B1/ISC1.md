# ISC1 - Input Service Distribution - Credit Memo Lines

- **Tabla:** ISC1
- **Descripción:** Input Service Distribution - Credit Memo Lines
- **Cantidad de campos:** 13
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ISC1.html

## Campos (13)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | [OISI](OISI.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `SourceType` | Source Document Type | Int | 11 | - |  | `18` = GST Tax Invoice<br>`19` = GST Credit Memo<br>`-18` = GST Debit Memo |
| 4 | `SourceNo` | Source Document No. | Int | 11 | - |  |  |
| 5 | `SrcEntry` | Source Document Entry | Int | 11 | - |  |  |
| 6 | `SrcStaType` | Source GST Tax Type | Int | 11 | - |  | `-100` = CGST<br>`-110` = SGST<br>`-120` = IGST<br>`-130` = Cess GST<br>`-150` = UTGST |
| 7 | `SrcTaxAcct` | Source Tax Account | nVarChar | 15 | - |  |  |
| 8 | `SACEntry` | SAC Entry | Int | 11 | - |  |  |
| 9 | `TarStaType` | Target GST Tax Type | Int | 11 | - |  | `-100` = CGST<br>`-110` = SGST<br>`-120` = IGST<br>`-130` = Cess GST<br>`-150` = UTGST |
| 10 | `TarTaxAcct` | Target Tax Account | nVarChar | 15 | - |  |  |
| 11 | `DistAmnt` | Credit Amount to Distribute | Num | 19.6 | - |  |  |
| 12 | `SrcSubType` | Source Document Subtype | nVarChar | 2 | - |  |  |
| 13 | `ITCType` | ITC Type | VarChar | 1 | - | E | `E` = Eligible<br>`I` = Ineligible |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum |
