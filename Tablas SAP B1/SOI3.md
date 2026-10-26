# SOI3 - Statement of Import - Invoices

- **Tabla:** SOI3
- **Descripción:** Statement of Import - Invoices
- **Cantidad de campos:** 19
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SOI3.html

## Campos (19)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WizardId` | Wizard ID | Int | 11 | - |  |  |
| 2 | `SOINum` | Statement No. | Int | 11 | - |  |  |
| 3 | `AgrNum` | Blanket Agreement No. | Int | 11 | - |  |  |
| 4 | `AgrNo` | Blanket Agreement Entry | Int | 11 | [OOAT](OOAT.md) |  |  |
| 5 | `CardCode` | Customer/Vendor Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 6 | `CardName` | Customer/Vendor Name | nVarChar | 200 | - |  |  |
| 7 | `PayToCtry` | BP Pay-to Country/Region | nVarChar | 3 | - |  |  |
| 8 | `PmntNum` | Payment No. | Int | 11 | - |  |  |
| 9 | `PmntEntry` | Payment Entry | Int | 11 | [OVPM](OVPM.md) |  |  |
| 10 | `PmntType` | Payment Type | Int | 11 | - |  |  |
| 11 | `PmntDate` | Payment Date | Date | 8 | - |  |  |
| 12 | `ExcBasSum` | Sum of Excise Base Amount | Num | 19.6 | - |  |  |
| 13 | `ExciseSum` | Sum of Excise Amount | Num | 19.6 | - |  |  |
| 14 | `VatBaseSum` | Sum of VAT Base Amount | Num | 19.6 | - |  |  |
| 15 | `VatSum` | Total of VAT | Num | 19.6 | - |  |  |
| 16 | `RegNo` | Registration No. | nVarChar | 18 | - |  |  |
| 17 | `RegDate` | Registration Date | Date | 8 | - |  |  |
| 18 | `ExecStat` | Execution Status | VarChar | 1 | - | S | `S` = Saved<br>`E` = Executed |
| 19 | `BPLId` | Branch | Int | 11 | [OBPL](OBPL.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WizardId, SOINum |
