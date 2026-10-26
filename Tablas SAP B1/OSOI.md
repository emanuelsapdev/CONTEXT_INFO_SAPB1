# OSOI - Statement of Import Wizard

- **Tabla:** OSOI
- **Descripción:** Statement of Import Wizard
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSOI.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WizardId` | Wizard ID | Int | 11 | - |  |  |
| 2 | `Name` | Name | nVarChar | 100 | - |  |  |
| 3 | `Date` | Run Date | Date | 8 | - |  |  |
| 4 | `UserSign` | User Signature | Int | 6 | - |  |  |
| 5 | `AgrNoFrom` | Agreement No. From | Int | 11 | - |  |  |
| 6 | `AgrNoTo` | Agreement No. To | Int | 11 | - |  |  |
| 7 | `PDateFrm` | Posting Date From | Date | 8 | - |  |  |
| 8 | `PDateTo` | Posting Date To | Date | 8 | - |  |  |
| 9 | `OrigWizId` | Original Wizard ID | Int | 11 | - |  |  |
| 10 | `OrigSOINum` | Original Statement No. | Int | 11 | - |  |  |
| 11 | `Status` | Status | VarChar | 1 | - | N | `N` = Created<br>`C` = Correction<br>`U` = Updated<br>`D` = Deleted |
| 12 | `CorrType` | Correction Type | VarChar | 1 | - |  | `R` = Replacement<br>`A` = Adjustment |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WizardId |
