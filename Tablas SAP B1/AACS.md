# AACS - Asset Classes - History

- **Tabla:** AACS
- **Descripción:** Asset Classes - History
- **Cantidad de campos:** 14
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AACS.html

## Campos (14)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Code | nVarChar | 20 | - |  |  |
| 2 | `Name` | Name | nVarChar | 100 | - |  |  |
| 3 | `AssetType` | Asset Type | VarChar | 1 | - | G | `G` = General<br>`L` = Low Value Asset |
| 4 | `LimitFrom` | Value Limit From | Num | 19.6 | - |  |  |
| 5 | `LimitTo` | Value Limit To | Num | 19.6 | - |  |  |
| 6 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 7 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 8 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 9 | `CreateDate` | Create Date | Date | 8 | - |  |  |
| 10 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 11 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 12 | `BPLId` | Branch | Int | 11 | [OBPL](OBPL.md) |  |  |
| 13 | `AttrGrp` | Attribute Group | Int | 11 | [OFAA](OFAA.md) | -1 |  |
| 14 | `SnapshotId` | Snapshot ID | Int | 11 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code, LogInstanc |
