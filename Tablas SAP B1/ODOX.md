# ODOX - Data Ownership - Exceptions

- **Tabla:** ODOX
- **Descripción:** Data Ownership - Exceptions
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ODOX.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `QueryId` | Query ID | nVarChar | 20 | - |  |  |
| 2 | `Object` | The Object Number | nVarChar | 20 | - |  |  |
| 3 | `SubObject` | Array Offset | Int | 6 | - | 0 |  |
| 4 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 5 | `UpdateUser` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 6 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 7 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 8 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Upgrade<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Auto Summary<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 9 | `AC` | Cache Access Counter | Int | 11 | - | 0 |  |
| 10 | `OwnerShpBy` | Defined by Ownership Method | VarChar | 1 | - | N | `N` = Not Specified<br>`R` = Ownership By Branch |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | QueryId, Object, SubObject, OwnerShpBy |
