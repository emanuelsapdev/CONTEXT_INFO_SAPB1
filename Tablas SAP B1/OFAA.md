# OFAA - Asset Attributes

- **Tabla:** OFAA
- **Descripción:** Asset Attributes
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OFAA.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Code | Int | 11 | - |  |  |
| 2 | `Name` | Name | nVarChar | 100 | - |  |  |
| 3 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 4 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 5 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 6 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 7 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 8 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 9 | `Locked` | Locked | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 10 | `SnapshotId` | Snapshot ID | Int | 11 | - | 0 |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code |
| Name | Yes | Name |
