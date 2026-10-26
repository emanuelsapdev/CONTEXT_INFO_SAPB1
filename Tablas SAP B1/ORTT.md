# ORTT - CPI and FC Rates

- **Tabla:** ORTT
- **Descripción:** CPI and FC Rates
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ORTT.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `RateDate` | Exchange Rate Date | Date | 8 | - |  |  |
| 2 | `Currency` | Currency Code | nVarChar | 3 | - |  |  |
| 3 | `Rate` | Currency Rate | Num | 19.6 | - |  |  |
| 4 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 5 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 6 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 7 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 8 | `UserSign2` | Updating User | Int | 11 | [OUSR](OUSR.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | RateDate, Currency |
| DATE | No | RateDate |
