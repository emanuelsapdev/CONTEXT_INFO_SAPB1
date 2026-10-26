# HFC2 - Hide Function Configuration - Rows

- **Tabla:** HFC2
- **Descripción:** Hide Function Configuration - Rows
- **Cantidad de campos:** 13
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/HFC2.html

## Campos (13)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `FuncID` | Function ID | Int | 11 | [OHFC](OHFC.md) |  |  |
| 3 | `MainMenu` | Main Menu ID | Int | 11 | - |  |  |
| 4 | `MovMenuTo` | Target Postion Menu Move | Int | 11 | - |  |  |
| 5 | `ActionType` | Action Type | Int | 6 | - | 0 | `0` = Hide Menu<br>`1` = Move Menu<br>`2` = Hide Pop-Up Menu |
| 6 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 7 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 8 | `Transfered` | Year Transfer [Y/N] | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 9 | `Instance` | Instance | Int | 6 | - | 0 |  |
| 10 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 11 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 12 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 13 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
