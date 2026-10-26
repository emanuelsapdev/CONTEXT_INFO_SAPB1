# WHT1 - Withholding Tax Definition

- **Tabla:** WHT1
- **Descripción:** Withholding Tax Definition
- **Cantidad de campos:** 25
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WHT1.html

## Campos (25)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WTCode` | WTax Code | nVarChar | 4 | [OWHT](OWHT.md) |  |  |
| 2 | `EffecDate` | Effective From | Date | 8 | - |  |  |
| 3 | `Rate` | Rate | Num | 19.6 | - |  |  |
| 4 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 5 | `TdsRate` | TDS Rate | Num | 19.6 | - |  |  |
| 6 | `SurRate` | Surcharge Rate | Num | 19.6 | - |  |  |
| 7 | `CessRate` | Cess Rate | Num | 19.6 | - |  |  |
| 8 | `HscRate` | HSC Rate | Num | 19.6 | - |  |  |
| 9 | `PmntTerms` | Payment Terms | Int | 6 | [OCTG](OCTG.md) |  |  |
| 10 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 11 | `IgstRate` | IGST Rate | Num | 19.6 | - |  |  |
| 12 | `CgstRate` | CGST Rate | Num | 19.6 | - |  |  |
| 13 | `SgstRate` | SGST Rate | Num | 19.6 | - |  |  |
| 14 | `UtgstRate` | UTGST Rate | Num | 19.6 | - |  |  |
| 15 | `CsgstRate` | Cess GST Rate | Num | 19.6 | - |  |  |
| 16 | `UomEntry` | UoM Entry | Int | 11 | [OUOM](OUOM.md) |  |  |
| 17 | `UoMCode` | UoM Code | nVarChar | 20 | - |  |  |
| 18 | `FixedAmnt` | Fixed Amount | Num | 19.6 | - |  |  |
| 19 | `Currency` | Fixed Amount Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 20 | `ItrNCRate` | TDS ITR Noncompliance Rate | Num | 19.6 | - |  |  |
| 21 | `PanNCRate` | TDS PAN Noncompliance Rate | Num | 19.6 | - |  |  |
| 22 | `Accumu` | Accumulation | VarChar | 1 | - | D | `D` = Daily<br>`M` = Monthly |
| 23 | `RdtParam1` | Reduction Calculation Parameter 1 | Num | 19.6 | - |  |  |
| 24 | `RdtParam2` | Reduction Calculation Parameter 2 | Num | 19.6 | - |  |  |
| 25 | `RdtCur` | Reduction Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WTCode, LineNum |
