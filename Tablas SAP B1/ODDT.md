# ODDT - Withholding Tax Deduction Hierarchy

- **Tabla:** ODDT
- **Descripción:** Withholding Tax Deduction Hierarchy
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ODDT.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Numerator` | Internal Number | Int | 11 | - |  |  |
| 2 | `CardCode` | BP Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 3 | `TrcCode` | Hierarchy Code | nVarChar | 10 | - |  |  |
| 4 | `TrcName` | Hierarchy Name | nVarChar | 30 | - |  |  |
| 5 | `DateFrom` | Valid From | Date | 8 | - |  |  |
| 6 | `DateTo` | Valid Until | Date | 8 | - |  |  |
| 7 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 8 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 9 | `LastUpdate` | Last Update Date | Date | 8 | - |  |  |
| 10 | `WHShaamGrp` | Withholding Shaam Group | VarChar | 1 | - | 1 | `1` = Services and Agriculture Products<br>`2` = Construction and Transportation<br>`3` = Insurance Commissions<br>`4` = Withholding Tax Instructions<br>`5` = Interest Exchange Rate Differences<br>`6` = Rental Fees |
| 11 | `DdctPrcnt` | Deduction % | Num | 19.6 | - |  |  |
| 12 | `MaxSum` | Maximum Total | Num | 19.6 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Numerator |
| CARD | Yes | CardCode, WHShaamGrp, TrcCode |
