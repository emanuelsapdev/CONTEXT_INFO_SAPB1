# DWZ1 - Dunning Wizard Array1 - BP Filter

- **Tabla:** DWZ1
- **Descripción:** Dunning Wizard Array1 - BP Filter
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/DWZ1.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WizardId` | Wizard ID | Int | 11 | [ODWZ](ODWZ.md) |  |  |
| 2 | `CardCode` | BP Card Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 3 | `DunAddr` | Dunning Address | nVarChar | 254 | - |  |  |
| 4 | `CheckedBP` | Checked BP | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 5 | `FaxNum` | Fax Number | nVarChar | 50 | - |  |  |
| 6 | `Email` | E-Mail Address | nVarChar | 100 | - |  |  |
| 7 | `DPPStatus` | Data Protection Status | VarChar | 1 | - | N | `N` = None<br>`D` = Erased |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WizardId, CardCode |
