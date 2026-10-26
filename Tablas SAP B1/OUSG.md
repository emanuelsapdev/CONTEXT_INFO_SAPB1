# OUSG - Usage of Nota Fiscal

- **Tabla:** OUSG
- **Descripción:** Usage of Nota Fiscal
- **Cantidad de campos:** 17
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OUSG.html

## Campos (17)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ID` | Usage ID | Int | 11 | - |  |  |
| 2 | `Usage` | Usage | nVarChar | 20 | - |  |  |
| 3 | `Locked` | Locked | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 4 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Auto Incr.<br>`D` = Data Doc.<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 5 | `UserSign` | User Signature | nVarChar | 6 | [OUSR](OUSR.md) |  |  |
| 6 | `PostTax` | Post Tax in Price to Stock | Int | 6 | - | 1 | `1` = Yes<br>`0` = No |
| 7 | `TaxOnly` | Tax Only | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `CFOPIIS` | CFOP Incoming In-State | nVarChar | 6 | [OCFP](OCFP.md) |  |  |
| 9 | `CFOPIOS` | CFOP Incoming Out-State | nVarChar | 6 | [OCFP](OCFP.md) |  |  |
| 10 | `CFOPII` | CFOP Incoming Import | nVarChar | 6 | [OCFP](OCFP.md) |  |  |
| 11 | `CFOPOIS` | CFOP Outgoing In-State | nVarChar | 6 | [OCFP](OCFP.md) |  |  |
| 12 | `CFOPOOS` | CFOP Outgoing Out-State | nVarChar | 6 | [OCFP](OCFP.md) |  |  |
| 13 | `CFOPOE` | CFOP Outgoing Export | nVarChar | 6 | [OCFP](OCFP.md) |  |  |
| 14 | `Descr` | Usage Description | nVarChar | 100 | - |  |  |
| 15 | `FreeChrgBP` | Free of Charge (BP) | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 16 | `ThirdParty` | Third Party | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 17 | `Adjustment` | Adjustment | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ID |
