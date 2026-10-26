# OTRT - Posting Templates

- **Tabla:** OTRT
- **Descripción:** Posting Templates
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OTRT.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TrtCode` | Template Code | nVarChar | 8 | - |  |  |
| 2 | `Dscription` | Template Description | nVarChar | 60 | - |  |  |
| 3 | `FrgnMode` | FC Template | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 4 | `Memo` | Details | nVarChar | 50 | - |  |  |
| 5 | `TransCode` | Transaction Code | nVarChar | 4 | - |  |  |
| 6 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 7 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 8 | `StampTax` | Stamp Tax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 9 | `AutoVat` | Automatic VAT | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 10 | `ManageWTax` | Manage WTax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 11 | `DeferedTax` | Deferred Tax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TrtCode |
