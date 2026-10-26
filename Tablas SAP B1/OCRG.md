# OCRG - Card Groups

- **Tabla:** OCRG
- **Descripción:** Card Groups
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCRG.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `GroupCode` | Group No. | Int | 6 | - |  |  |
| 2 | `GroupName` | Group Name | nVarChar | 100 | - |  |  |
| 3 | `GroupType` | Group Type | VarChar | 1 | - | C | `C` = Customer Group<br>`S` = Vendor Group |
| 4 | `Locked` | Locked | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 5 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 6 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 7 | `PriceList` | Price List | Int | 6 | [OPLN](OPLN.md) |  |  |
| 8 | `DiscRel` | Effective Discount Groups | VarChar | 1 | - | L | `L` = Lowest Discount<br>`H` = Highest Discount<br>`A` = Average<br>`S` = Total<br>`M` = Discount Multiples |
| 9 | `EffecPrice` | Effective Price | VarChar | 1 | - | D | `D` = Default Priority<br>`L` = Lowest Price<br>`H` = Highest Price |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | GroupCode |
| GROUP_TYPE | No | GroupType |
| GROUP_NAME | Yes | GroupName |
