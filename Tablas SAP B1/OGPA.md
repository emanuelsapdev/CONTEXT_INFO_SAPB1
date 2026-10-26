# OGPA - Gross Profit Adjustment

- **Tabla:** OGPA
- **Descripción:** Gross Profit Adjustment
- **Cantidad de campos:** 13
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OGPA.html

## Campos (13)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | - |  |  |
| 2 | `Name` | Gross Profit Adjustment Name | nVarChar | 100 | - |  |  |
| 3 | `CreateDate` | Create Date | Date | 8 | - |  |  |
| 4 | `UserSign` | User Signature | Int | 6 | - |  |  |
| 5 | `Status` | Status | VarChar | 1 | - |  | `R` = Saved Recommendations<br>`S` = Simulation<br>`E` = Executed<br>`P` = Saved Parameters |
| 6 | `Remarks` | Description | nVarChar | 254 | - |  |  |
| 7 | `WizType` | Wizard Type | VarChar | 1 | - | A | `A` = Gross Profit Adjustment Wizard<br>`R` = Production Cost Recalculation Wizard |
| 8 | `nGPAdj` | Number of Gross Profits Recalculated | Int | 11 | - |  |  |
| 9 | `nPCAdj` | Number of Product Costs Recalculated | Int | 11 | - |  |  |
| 10 | `nGPFail` | Number of Gross Profit Recalculations Failed | Int | 11 | - |  |  |
| 11 | `nPCFail` | Number of Failed Product Cost Recalculations | Int | 11 | - |  |  |
| 12 | `nJECreate` | Number of Journal Entries Created | Int | 11 | - |  |  |
| 13 | `nMRVCreate` | Number of MRV Created | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
