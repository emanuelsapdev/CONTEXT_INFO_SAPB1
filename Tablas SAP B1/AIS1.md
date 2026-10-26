# AIS1 - Input Service Distribution - Rows

- **Tabla:** AIS1
- **Descripción:** Input Service Distribution - Rows
- **Cantidad de campos:** 14
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AIS1.html

## Campos (14)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | [OISD](OISD.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `SourceType` | Source Document Type | Int | 11 | - |  | `18` = GST Tax Invoice<br>`19` = GST Credit Memo<br>`-18` = GST Debit Memo |
| 4 | `SourceNo` | Source Document No. | Int | 11 | - |  |  |
| 5 | `SrcEntry` | Source Document Entry | Int | 11 | - |  |  |
| 6 | `SrcLocCode` | Source Location Code | Int | 11 | [OLCT](OLCT.md) |  |  |
| 7 | `SrcLocName` | Source Location Name | nVarChar | 100 | - |  |  |
| 8 | `SrcStaType` | Source GST Tax Type | Int | 11 | - |  | `-100` = CGST<br>`-110` = SGST<br>`-120` = IGST<br>`-130` = Cess GST<br>`-150` = UTGST |
| 9 | `SrcTaxAcct` | Source Tax Account | nVarChar | 15 | - |  |  |
| 10 | `SACEntry` | SAC Entry | Int | 11 | - |  |  |
| 11 | `CrdtAmnt` | Total Credit Amount | Num | 19.6 | - |  |  |
| 12 | `DistAmnt` | Credit Amount to Distribute | Num | 19.6 | - |  |  |
| 13 | `SrcSubType` | Source Document Subtype | nVarChar | 2 | - |  |  |
| 14 | `ITCType` | ITC Type | VarChar | 1 | - | E | `E` = Eligible<br>`I` = Ineligible |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum |
