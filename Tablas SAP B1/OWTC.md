# OWTC - WTax Certificates

- **Tabla:** OWTC
- **Descripción:** WTax Certificates
- **Cantidad de campos:** 19
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OWTC.html

## Campos (19)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `RctType` | Object Type | nVarChar | 20 | - |  | `24` = Incoming Payment<br>`46` = Outgoing Payment |
| 3 | `RctAbs` | Receipt No. | Int | 11 | - |  |  |
| 4 | `Jurisdict` | Jurisdiction | nVarChar | 2 | - |  |  |
| 5 | `WtaxType` | WTax Type | nVarChar | 2 | - |  | `--` = WTax Certificate<br>`OV` = Outgoing VAT - Withholding Tax<br>`OG` = Outgoing Gross Income - Withholding Tax<br>`ON` = Outgoing Income - Withholding Tax<br>`OS` = Outgoing Social Security - Withholding Tax<br>`OI` = Outgoing Industry Specific - Withholding Tax<br>`OD` = Outgoing District Specific - Withholding Tax<br>`IC` = Incoming WTax Certificate |
| 6 | `WtAbsEntry` | Internal Number | Int | 11 | - |  |  |
| 7 | `DueDate` | Due Date | Date | 8 | - |  |  |
| 8 | `CerSeries` | WTax Certificate Series | Int | 11 | - |  |  |
| 9 | `Number` | Number | Int | 11 | - |  |  |
| 10 | `RefNumber` | Reference Number | nVarChar | 20 | - |  |  |
| 11 | `SumVatAmnt` | Sum of VAT Amount | Num | 19.6 | - |  |  |
| 12 | `SumDocTot` | Sum of Doc. Total Amount | Num | 19.6 | - |  |  |
| 13 | `SumBaseAmn` | Sum of Base Amount | Num | 19.6 | - |  |  |
| 14 | `SumAccumAm` | Sum of Accumulated Amount | Num | 19.6 | - |  |  |
| 15 | `SumPercpAm` | Sum of Perception Amount | Num | 19.6 | - |  |  |
| 16 | `PTICode` | POI Code | nVarChar | 5 | - |  |  |
| 17 | `Handwrtten` | Manual Numbering | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 18 | `PIndicator` | Period Indicator | nVarChar | 10 | - | ' ' |  |
| 19 | `PTICodeRef` | POI Code Reference | nVarChar | 20 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
