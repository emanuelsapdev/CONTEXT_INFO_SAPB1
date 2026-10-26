# ABFC - Bin Field Configuration - History

- **Tabla:** ABFC
- **Descripción:** Bin Field Configuration - History
- **Cantidad de campos:** 14
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ABFC.html

## Campos (14)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `FldType` | Field Type | VarChar | 1 | - |  | `S` = Warehouse Sublevel<br>`A` = Bin Location Attribute |
| 3 | `FldNum` | Field Number | Int | 6 | - |  |  |
| 4 | `DispName` | Display Name | nVarChar | 20 | - |  |  |
| 5 | `Activated` | Active [Y/N] | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 7 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 8 | `Transfered` | Year Transfer [Y/N] | VarChar | 1 | - | N |  |
| 9 | `Instance` | Instance | Int | 6 | - | 0 |  |
| 10 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 11 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 12 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 13 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 14 | `DftName` | Default Field Name | nVarChar | 20 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LogInstanc |
