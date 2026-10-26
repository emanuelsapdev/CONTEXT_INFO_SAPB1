# APRC - Cost Center

- **Tabla:** APRC
- **Descripción:** Cost Center
- **Cantidad de campos:** 16
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/APRC.html

## Campos (16)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `PrcCode` | Center Code | nVarChar | 8 | - |  |  |
| 2 | `PrcName` | Center Name | nVarChar | 30 | - |  |  |
| 3 | `GrpCode` | Group Code | nVarChar | 4 | - |  |  |
| 4 | `Balance` | Balance | Num | 19.6 | - |  |  |
| 5 | `Locked` | Locked | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 7 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 8 | `DimCode` | In Which Dimension | Int | 6 | [ODIM](ODIM.md) | 1 |  |
| 9 | `CCTypeCode` | Cost Center Type Code | nVarChar | 8 | [OCCT](OCCT.md) |  |  |
| 10 | `ValidFrom` | Valid From | Date | 8 | - |  |  |
| 11 | `ValidTo` | Valid To | Date | 8 | - |  |  |
| 12 | `Active` | Active | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 13 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 14 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 15 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 16 | `CCOwner` | Cost Center Owner | Int | 11 | [OHEM](OHEM.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | PrcCode, LogInstanc |
