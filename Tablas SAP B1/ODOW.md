# ODOW - Data Ownership - Objects

- **Tabla:** ODOW
- **Descripción:** Data Ownership - Objects
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ODOW.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Object` | The Object Number | nVarChar | 20 | - |  |  |
| 2 | `SubObject` | Array Offset | Int | 6 | - | 0 |  |
| 3 | `OwnerField` | Column Number of Owner | Int | 6 | - |  |  |
| 4 | `Active` | Indication: Does it Work | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 5 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 6 | `UpdateUser` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 7 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 8 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 9 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Upgrade<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Auto Summary<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 10 | `AC` | Cache Access Counter | Int | 11 | - | 0 |  |
| 11 | `OwnerCtrl` | The way owner is controlled | Int | 6 | - | 7 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Object, SubObject |
