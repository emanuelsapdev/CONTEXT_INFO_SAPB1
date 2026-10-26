# ODSW - SN Draft Attribs in Location

- **Tabla:** ODSW
- **Descripción:** SN Draft Attribs in Location
- **Cantidad de campos:** 14
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ODSW.html

## Campos (14)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ItemCode` | Item Code | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 2 | `SysNumber` | System No. | Int | 11 | [OSRN](OSRN.md) |  |  |
| 3 | `WhsCode` | Warehouse Code | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 4 | `Location` | Loc. | nVarChar | 100 | - |  |  |
| 5 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 6 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 7 | `Transfered` | Transferred | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `Instance` | Instance | Int | 6 | - | 0 |  |
| 9 | `AbsEntry` | abs entry | Int | 11 | - |  |  |
| 10 | `MdAbsEntry` | MD Abs Entry | Int | 11 | - |  |  |
| 11 | `ObjType` | Object Type | nVarChar | 20 | - |  |  |
| 12 | `LogInstanc` | Log Instance | Int | 11 | - |  |  |
| 13 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 14 | `UpdateDate` | Update Date | Date | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
