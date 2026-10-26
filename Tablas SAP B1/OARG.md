# OARG - Customs Groups

- **Tabla:** OARG
- **Descripción:** Customs Groups
- **Cantidad de campos:** 16
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OARG.html

## Campos (16)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CstGrpCode` | Code | Int | 6 | - |  |  |
| 2 | `CstGrpName` | Name | nVarChar | 20 | - |  |  |
| 3 | `GroupNum` | Number | nVarChar | 20 | - |  |  |
| 4 | `Custom` | Customs | Num | 19.6 | - |  |  |
| 5 | `BuyTax` | Purchase | Num | 19.6 | - |  |  |
| 6 | `OtherTax` | Other | Num | 19.6 | - |  |  |
| 7 | `TotalTax` | Total | Num | 19.6 | - |  |  |
| 8 | `Locked` | Locked | VarChar | 1 | - | N | `N` = Changeable<br>`Y` = Locked |
| 9 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 10 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 11 | `cstAllcAcc` | Customs Allocation Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 12 | `cstExpAcc` | Customs Expense Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 13 | `PortAddr` | Local Clearance - Port Address | nVarChar | 50 | - |  |  |
| 14 | `PortState` | Port State | nVarChar | 3 | - |  |  |
| 15 | `ExciExpAcc` | Excise Expense Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 16 | `ExciAlcAcc` | Excise Allocation Account | nVarChar | 15 | [OACT](OACT.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CstGrpCode |
| GROUP_NAME | Yes | CstGrpName |
