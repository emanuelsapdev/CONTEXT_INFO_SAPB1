# OUGP - UoM Group

- **Tabla:** OUGP
- **Descripción:** UoM Group
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OUGP.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `UgpEntry` | UoM Group Abs. Entry | Int | 11 | - |  |  |
| 2 | `UgpCode` | UoM Group Code | nVarChar | 20 | - |  |  |
| 3 | `UgpName` | UoM Group Name | nVarChar | 100 | - |  |  |
| 4 | `BaseUom` | Base UoM Abs. Entry | Int | 11 | [OUOM](OUOM.md) |  |  |
| 5 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 6 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 7 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 8 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 9 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 10 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 11 | `Locked` | Locked | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | UgpEntry |
| CODE | Yes | UgpCode |
| NAME | No | UgpName |
