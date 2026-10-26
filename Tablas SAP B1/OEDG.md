# OEDG - Discount Groups

- **Tabla:** OEDG
- **Descripción:** Discount Groups
- **Cantidad de campos:** 14
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OEDG.html

## Campos (14)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Unique Entry | Int | 11 | - |  |  |
| 2 | `Type` | Type | VarChar | 1 | - |  | `A` = All BPs<br>`C` = Customer Group<br>`V` = Vendor Group<br>`S` = Specific BP |
| 3 | `ObjType` | Object Type | nVarChar | 20 | - | -1 | `-1`<br>`10` = Card Payment Groups<br>`2` = Cards |
| 4 | `ObjCode` | Object Code | nVarChar | 15 | - |  |  |
| 5 | `DiscRel` | Disc. Relations | VarChar | 1 | - | L | `L` = Lowest Discount<br>`H` = Highest Discount<br>`A` = Average<br>`S` = Total<br>`M` = Discount Multiples |
| 6 | `ValidFor` | Active | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 7 | `ValidForm` | Active From | Date | 8 | - |  |  |
| 8 | `ValidTo` | Active To | Date | 8 | - |  |  |
| 9 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 10 | `UserSign` | User Form | Int | 6 | [OUSR](OUSR.md) |  |  |
| 11 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 12 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 13 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 14 | `UpdateDate` | Update Date | Date | 8 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| CODE_TYPE | Yes | ObjCode, Type |
