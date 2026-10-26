# OCDT - Credit Card Payment

- **Tabla:** OCDT
- **Descripción:** Credit Card Payment
- **Cantidad de campos:** 23
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCDT.html

## Campos (23)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Credit Card Payment Code | nVarChar | 8 | - |  |  |
| 2 | `Name` | Credit Card Payment Name | nVarChar | 30 | - |  |  |
| 3 | `TERM_TYPE` | Credit Card Payment Types | VarChar | 1 | - | F | `D` = By Dates<br>`F` = After Time Period |
| 4 | `After_Days` | Payment After Days | Int | 6 | - |  |  |
| 5 | `After_Mnth` | Payment After Months | Int | 6 | - |  |  |
| 6 | `Day_From1` | From Day 1 | Int | 6 | - |  |  |
| 7 | `Day_To1` | To Day 1 | Int | 6 | - |  |  |
| 8 | `Pay_Day1` | Payment Date 1 | Int | 6 | - |  |  |
| 9 | `Pay_Month1` | No. of Months 1 | Int | 6 | - |  |  |
| 10 | `Day_From2` | From Day 2 | Int | 6 | - |  |  |
| 11 | `Day_To2` | To Day 2 | Int | 6 | - |  |  |
| 12 | `Pay_Day2` | Payment Date 2 | Int | 6 | - |  |  |
| 13 | `Pay_Month2` | No. of Months 2 | Int | 6 | - |  |  |
| 14 | `Day_From3` | From Day 3 | Int | 6 | - |  |  |
| 15 | `Day_To3` | To Day 3 | Int | 6 | - |  |  |
| 16 | `Pay_Day3` | Payment Date 3 | Int | 6 | - |  |  |
| 17 | `Pay_Month3` | No. of Months 3 | Int | 6 | - |  |  |
| 18 | `Day_From4` | From Day 4 | Int | 6 | - |  |  |
| 19 | `Day_To4` | To Day 4 | Int | 6 | - |  |  |
| 20 | `Pay_Day4` | Payment Date 4 | Int | 6 | - |  |  |
| 21 | `Pay_Month4` | No. of Months 4 | Int | 6 | - |  |  |
| 22 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 23 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code |
