# SOI5 - Statement of Import - Lines

- **Tabla:** SOI5
- **Descripción:** Statement of Import - Lines
- **Cantidad de campos:** 30
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SOI5.html

## Campos (30)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WizardId` | Wizard ID | Int | 11 | - |  |  |
| 2 | `SOINum` | Statement No. | Int | 11 | - |  |  |
| 3 | `DocType` | Document Type | Int | 11 | - |  |  |
| 4 | `DocEntry` | Document Abs Entry | Int | 11 | - |  |  |
| 5 | `SOILineNum` | SOI Line No. | Int | 11 | - |  |  |
| 6 | `DocLineNum` | Line No. | Int | 11 | - |  |  |
| 7 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 8 | `ItemName` | Item Description | nVarChar | 200 | - |  |  |
| 9 | `unitMsr` | UoM Name | nVarChar | 100 | - |  |  |
| 10 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 11 | `TotalFrgn` | Total (Doc.) | Num | 19.6 | - |  |  |
| 12 | `LineTotal` | Total (LC) | Num | 19.6 | - |  |  |
| 13 | `Currency` | Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 14 | `Rate` | Line Rate | Num | 19.6 | - |  |  |
| 15 | `BaseRate` | Base Currency Rate | Num | 19.6 | - |  |  |
| 16 | `BasNumAtCr` | Base Ref. Vendor Ref. No. | nVarChar | 200 | - |  |  |
| 17 | `BaseDocNum` | Base Ref. No. | Int | 11 | - |  |  |
| 18 | `BaseEntry` | Base Entry | Int | 11 | - |  |  |
| 19 | `BasTaxDate` | Base Ref. Document Date | Date | 8 | - |  |  |
| 20 | `FExcBasSum` | Fixed Excise Base Amount | Num | 19.6 | - |  |  |
| 21 | `AExcBasSum` | Ad Valorem Excise Base Amount | Num | 19.6 | - |  |  |
| 22 | `ExciseUoM` | Excise Units of Measure | Int | 11 | - |  | `112` = Liters (m3)<br>`168` = Tons, metric tons (1000 kg)<br>`251` = Horsepower (1 hp = 0.75 kW)<br>`831` = Liters of anhydrous (pure) alcohol |
| 23 | `ExcRateUoM` | Excise Rate Units of Measure | Num | 19.6 | - |  |  |
| 24 | `ExcRateAdV` | Excise Rate Ad Valorem | Num | 19.6 | - |  |  |
| 25 | `ExciseSum` | Excise Amount | Num | 19.6 | - |  |  |
| 26 | `VatBaseSum` | VAT Base Amount | Num | 19.6 | - |  |  |
| 27 | `VatPrcnt` | VAT Rate per Row | Num | 19.6 | - |  |  |
| 28 | `VatSum` | VAT Amount | Num | 19.6 | - |  |  |
| 29 | `TaxCtgr` | Tax Type (Annual List) | nVarChar | 6 | - |  |  |
| 30 | `VatGroup` | VAT Code | nVarChar | 8 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WizardId, SOINum, DocType, DocEntry, DocLineNum |
| SOILINENUM | Yes | WizardId, SOINum, SOILineNum |
