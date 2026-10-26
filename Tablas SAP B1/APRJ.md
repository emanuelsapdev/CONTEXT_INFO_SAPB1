# APRJ - Project Codes

- **Tabla:** APRJ
- **Descripción:** Project Codes
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/APRJ.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `PrjCode` | Project Code | nVarChar | 20 | - |  |  |
| 2 | `PrjName` | Project Name | nVarChar | 100 | - |  |  |
| 3 | `Locked` | Locked | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 4 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 5 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 6 | `ValidFrom` | Valid From | Date | 8 | - |  |  |
| 7 | `ValidTo` | Valid To | Date | 8 | - |  |  |
| 8 | `Active` | Active | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 9 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 10 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 11 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 12 | `DTVId` | Datev Identifier | nVarChar | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | PrjCode, LogInstanc |
