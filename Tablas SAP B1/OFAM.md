# OFAM - Fixed Asset Data Migration

- **Tabla:** OFAM
- **Descripción:** Fixed Asset Data Migration
- **Cantidad de campos:** 13
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OFAM.html

## Campos (13)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WizardId` | Wizard ID | Int | 11 | - |  |  |
| 2 | `WizardName` | Migration Run Name | nVarChar | 100 | - |  |  |
| 3 | `CreateDate` | Migration Run Date | Date | 8 | - |  |  |
| 4 | `AcctDtn` | Migrate Account Determination | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 5 | `DprArea` | Migrate Depreciation Areas | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 6 | `DprType` | Migrate Depreciation Types | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 7 | `AssetClass` | Migrate Asset Classes | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 8 | `AssetNum` | Migrate Asset Numbering | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 9 | `AssetItem` | Migrate Asset Items | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 10 | `UpdExstItm` | Overwrite Existing Data | VarChar | 1 | - | N | `Y` = Overwrite Existing Data<br>`N` = Skip if Data Already Exists |
| 11 | `Status` | Status of Migration Run | VarChar | 1 | - | S | `S` = Successful<br>`P` = Partially Successful<br>`F` = Failed |
| 12 | `Remarks` | Remarks | nVarChar | 254 | - |  |  |
| 13 | `FiscalYear` | Migration Data to Fiscal Year | nVarChar | 10 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WizardId |
