# OTRC - Journal Entry Codes

- **Tabla:** OTRC
- **Descripción:** Journal Entry Codes
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OTRC.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TrnsCode` | Code | nVarChar | 4 | - |  |  |
| 2 | `TrnsCodDsc` | Description | nVarChar | 20 | - |  |  |
| 3 | `Locked` | Locked | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 4 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 5 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 6 | `Pcn874Ctg` | Trans. Category for PCN874 | VarChar | 1 | - | N | `N` = None<br>`I` = Import Log<br>`E` = Export Log<br>`O` = Other<br>`R` = A/R Invoice - Palestinian Territory<br>`P` = A/P Invoice - Palestinian Territory<br>`M` = Self-Employed - Sales<br>`C` = Self-Employed - Purchase |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TrnsCode |
| DESCRIP | No | TrnsCodDsc |
