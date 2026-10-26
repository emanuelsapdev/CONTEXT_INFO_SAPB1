# OHFC - Hide Functions Configuration

- **Tabla:** OHFC
- **Descripción:** Hide Functions Configuration
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OHFC.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `FuncName` | Function Name | nVarChar | 100 | - |  |  |
| 3 | `Hidden` | Enabled [Y/N] | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 4 | `Type` | Type | nVarChar | 6 | - | 0 | `0` = System<br>`1` = User |
| 5 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 6 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 7 | `Transfered` | Year Transfer [Y/N] | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `Instance` | Instance | Int | 6 | - | 0 |  |
| 9 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 10 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 11 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 12 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
