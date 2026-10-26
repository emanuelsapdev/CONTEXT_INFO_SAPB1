# OBCD - Bar Code Master Data

- **Tabla:** OBCD
- **Descripción:** Bar Code Master Data
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OBCD.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `BcdEntry` | Bar Code Abs. Entry | Int | 11 | - |  |  |
| 2 | `BcdCode` | Bar Code - Code | nVarChar | 254 | - |  |  |
| 3 | `BcdName` | Bar Code Name | nVarChar | 100 | - |  |  |
| 4 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 5 | `UomEntry` | UoM Abs. Entry | Int | 11 | [OUOM](OUOM.md) |  |  |
| 6 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 7 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 8 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 9 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 10 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 11 | `CreateDate` | Creation Date | Date | 8 | - |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | BcdEntry |
| ITEM | Yes | ItemCode, UomEntry, BcdCode |
| BCD_CODE | No | BcdCode |
