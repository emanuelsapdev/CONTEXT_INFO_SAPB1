# AHF1 - Hide Functions Configuration - Rows History

- **Tabla:** AHF1
- **Descripción:** Hide Functions Configuration - Rows History
- **Cantidad de campos:** 17
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AHF1.html

## Campos (17)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `FuncID` | Function ID | Int | 11 | [OHFC](OHFC.md) |  |  |
| 3 | `formNum` | Form Number | nVarChar | 128 | - |  |  |
| 4 | `ItemUID` | Item UID | nVarChar | 128 | - |  |  |
| 5 | `ColUID` | Column UID | nVarChar | 128 | - |  |  |
| 6 | `HideVal` | Hide Valid Value | nVarChar | 20 | - |  |  |
| 7 | `AltVal` | Alternative Valid Value | nVarChar | 20 | - |  |  |
| 8 | `PanelID` | Hide Item by Panel | Int | 6 | - |  |  |
| 9 | `ActionType` | Hide Item Action Type | Int | 6 | - | 0 | `0` = Hide Item<br>`1` = Hide Column<br>`2` = Hide Item's Valid Value<br>`3` = Hide Panel<br>`4` = Hide Column's Valid Value |
| 10 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 11 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 12 | `Transfered` | Year Transfer [Y/N] | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 13 | `Instance` | Instance | Int | 6 | - | 0 |  |
| 14 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 15 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 16 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 17 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LogInstanc |
