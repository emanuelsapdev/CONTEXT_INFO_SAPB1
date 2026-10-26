# ISW2 - Intrastat Reported Items

- **Tabla:** ISW2
- **Descripción:** Intrastat Reported Items
- **Cantidad de campos:** 19
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ISW2.html

## Campos (19)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WizAbsEnt` | Wizard Run Key | Int | 11 | [OISW](OISW.md) |  |  |
| 2 | `ItemCode` | Item Code | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 3 | `CommCode` | Commodity Code | nVarChar | 12 | - |  |  |
| 4 | `SerCode` | Service Code | nVarChar | 12 | - |  |  |
| 5 | `AddMUnit` | Additional Measure Unit | nVarChar | 50 | - |  |  |
| 6 | `FactorAM` | Factor Additional Measure | Num | 19.6 | - |  |  |
| 7 | `OriRegSta` | Region of Origin (for Export) | nVarChar | 12 | - |  |  |
| 8 | `DstRegSta` | Destination Region (Import) | nVarChar | 12 | - |  |  |
| 9 | `CtryOrig` | Country/Region of Origin | nVarChar | 3 | - |  |  |
| 10 | `SerSupplM` | Service Supply Method | nVarChar | 12 | - | I | `I` = Immediate<br>`R` = To More Resumptions |
| 11 | `SerPymMeth` | Service Payment Method | nVarChar | 12 | - | X | `A` = Accredited to Bank Account<br>`B` = Bank Transfer<br>`X` = Other |
| 12 | `ItemType` | Item Type | VarChar | 1 | - | I | `I` = Item<br>`S` = Service<br>`N` = Item not relevant to Intrastat |
| 13 | `ItemName` | Item Name | nVarChar | 200 | - |  |  |
| 14 | `DestRegCry` | Destination Country - Region | nVarChar | 3 | - |  |  |
| 15 | `OrigRegCry` | Origin Region Country | nVarChar | 3 | - |  |  |
| 16 | `UseWeight` | Use Wt in Add. Measure Calc. | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 17 | `StatCode` | Statistical Code | nVarChar | 2 | - |  |  |
| 18 | `NatOfTrans` | Nature of Transaction | nVarChar | 50 | - |  |  |
| 19 | `StatProc` | Statistical Procedure | nVarChar | 50 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WizAbsEnt, ItemCode |
