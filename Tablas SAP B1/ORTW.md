# ORTW - Boleto Retorno Wizard: Parameter Sets

- **Tabla:** ORTW
- **Descripción:** Boleto Retorno Wizard: Parameter Sets
- **Cantidad de campos:** 13
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ORTW.html

## Campos (13)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `WDueDtFrom` | Due Date From | Date | 8 | - |  |  |
| 3 | `WDueDtTo` | Due Date To | Date | 8 | - |  |  |
| 4 | `WImpFile` | Import File | Text | 16 | - |  |  |
| 5 | `WMatching` | Boleto Matching | Int | 11 | - |  |  |
| 6 | `WBoletosAu` | Boletos Automatic Count | Int | 11 | - |  |  |
| 7 | `WBoletosMn` | Boletos Manual Count | Int | 11 | - |  |  |
| 8 | `WBoletosNI` | Boletos Not Identified Count | Int | 11 | - |  |  |
| 9 | `WRelDate` | Release Date | Date | 8 | - |  |  |
| 10 | `WCollDisc` | Collection or Discounted | Int | 11 | - |  |  |
| 11 | `WBankAcc1` | Bank Acct No. 1 | nVarChar | 50 | - |  |  |
| 12 | `WBankAcc2` | Bank Acct No. 2 | nVarChar | 50 | - |  |  |
| 13 | `WFileForm2` | File Format 2 | nVarChar | 50 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
