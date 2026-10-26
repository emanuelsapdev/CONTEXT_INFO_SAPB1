# IPF2 - Landed Costs - Costs

- **Tabla:** IPF2
- **Descripción:** Landed Costs - Costs
- **Cantidad de campos:** 19
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/IPF2.html

## Campos (19)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Landed Costs Internal ID | Int | 11 | [OIPF](OIPF.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `AlcCode` | Cost Code | nVarChar | 2 | [OALC](OALC.md) |  |  |
| 4 | `OhType` | Load by | VarChar | 1 | - |  | `F` = Cash Value Before Customs<br>`C` = Cash Value After Customs<br>`Q` = Quantity<br>`W` = Weight<br>`V` = Volume<br>`A` = Equal<br>`L` = Legal Cost |
| 5 | `CostSum` | Total Costs | Num | 19.6 | - |  |  |
| 6 | `CostSumFC` | Total Costs (FC) | Num | 19.6 | - |  |  |
| 7 | `Factor` | Factor | Num | 19.6 | - |  |  |
| 8 | `CostType` | Cost Type | VarChar | 1 | - | F | `F` = Fixed Costs<br>`V` = Variable Costs<br>`L` = Legal Costs |
| 9 | `Locked` | Locked | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 10 | `LaCAllcAcc` | Landed Costs Alloc. Account | nVarChar | 15 | - |  |  |
| 11 | `CostSumSC` | Total Costs (SC) | Num | 19.6 | - |  |  |
| 12 | `InCustCalc` | Included in Customs Calc | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 13 | `OpenCost` | Open Costs | Num | 19.6 | - |  |  |
| 14 | `OpenCostFC` | Open Costs (FC) | Num | 19.6 | - |  |  |
| 15 | `OpenCostSC` | Open Costs (SC) | Num | 19.6 | - |  |  |
| 16 | `AgentCode` | Subst. Code | nVarChar | 15 | - |  |  |
| 17 | `AgentName` | Subst. Name | nVarChar | 100 | - |  |  |
| 18 | `CostCateg` | Cost Category | VarChar | 1 | - |  | `V` = Customs VAT<br>`E` = Excise Cost<br>`D` = Customs Duty |
| 19 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, AlcCode, CostType |
| NUM | No | DocEntry, LineNum |
