# OALC - Loading Expenses

- **Tabla:** OALC
- **Descripción:** Loading Expenses
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OALC.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AlcCode` | Code | nVarChar | 2 | - |  |  |
| 2 | `AlcName` | Name | nVarChar | 30 | - |  |  |
| 3 | `OhType` | Allocation By | VarChar | 1 | - | F | `F` = Cash Value Before Customs<br>`C` = Cash Value After Customs<br>`Q` = Quantity<br>`W` = Weight<br>`V` = Volume<br>`A` = Equal<br>`L` = Legal Cost |
| 4 | `AcctCode` | Account Code | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 5 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Data Doc.<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 6 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 7 | `LaCAllcAcc` | Landed Costs Alloc. Account | nVarChar | 15 | - |  |  |
| 8 | `CostCateg` | Cost Category | VarChar | 1 | - |  | `V` = Customs VAT<br>`E` = Excise Cost<br>`D` = Customs Duty |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AlcCode |
| GROUP_NAME | No | AlcName |
