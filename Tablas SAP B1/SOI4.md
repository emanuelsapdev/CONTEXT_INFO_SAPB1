# SOI4 - Statement of Import - Invoices

- **Tabla:** SOI4
- **Descripción:** Statement of Import - Invoices
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SOI4.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WizardId` | Wizard ID | Int | 11 | - |  |  |
| 2 | `SOINum` | Statement No. | Int | 11 | - |  |  |
| 3 | `DocType` | Document Type | Int | 11 | - |  |  |
| 4 | `DocEntry` | Document Abs Entry | Int | 11 | - |  |  |
| 5 | `DocNum` | Doc. No. | Int | 11 | - |  |  |
| 6 | `DocDate` | Posting Date | Date | 8 | - |  |  |
| 7 | `TaxDate` | Document Date | Date | 8 | - |  |  |
| 8 | `NumAtCard` | BP Reference No. | nVarChar | 200 | - |  |  |
| 9 | `InvEntry` | Invoice Abs Entry | Int | 11 | [OINV](OINV.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WizardId, SOINum, DocType, DocEntry |
