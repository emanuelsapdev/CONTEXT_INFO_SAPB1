# ACEM - Cost Element

- **Tabla:** ACEM
- **Descripción:** Cost Element
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ACEM.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CemCode` | Cost Element Code | nVarChar | 20 | - |  |  |
| 2 | `CemDescr` | Cost Element Description | nVarChar | 50 | - |  |  |
| 3 | `Active` | Active | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 4 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 256000005 |  |
| 5 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 6 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 7 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 8 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 9 | `CreateTS` | Creatn Time - Incl. Secs | Int | 11 | - |  |  |
| 10 | `UpdateTS` | Update Full Time | Int | 11 | - |  |  |
| 11 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CemCode, LogInstanc |
