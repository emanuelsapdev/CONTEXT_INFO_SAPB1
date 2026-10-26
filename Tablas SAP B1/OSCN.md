# OSCN - Customer/Vendor Cat. No.

- **Tabla:** OSCN
- **Descripción:** Customer/Vendor Cat. No.
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSCN.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 2 | `CardCode` | BP Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 3 | `Substitute` | BP Catalog Number | nVarChar | 50 | - |  |  |
| 4 | `Transfered` | Postponed to Next Year | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 5 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 6 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 7 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 8 | `ShowSCN` | Display BP Catalog Number | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 9 | `IsDefault` | Is Default BP Catalog | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 10 | `Descriptio` | BP Catalog Description | nVarChar | 200 | - |  |  |
| 11 | `DataVers` | Data Version | Int | 11 | - | 1 |  |

## Claves e índices (6)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ItemCode, CardCode, Substitute |
| CARD_SCN | No | CardCode, Substitute |
| CARD | No | CardCode, ItemCode |
| ITEM | No | ItemCode, CardCode |
| SUBSTITUTE | No | Substitute |
| DEFAULT | No | CardCode, ItemCode, IsDefault |
