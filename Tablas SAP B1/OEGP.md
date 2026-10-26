# OEGP - E-Mail Group

- **Tabla:** OEGP
- **Descripción:** E-Mail Group
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OEGP.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `EmlGrpCode` | E-Mail Group Code | nVarChar | 20 | - |  |  |
| 2 | `EmlGrpName` | E-Mail Group Name | nVarChar | 100 | - |  |  |
| 3 | `Locked` | Locked | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 4 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 5 | `UserSign` | User Signature | Int | 11 | [OUSR](OUSR.md) |  |  |
| 6 | `LogInstanc` | Log Instance | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | EmlGrpCode |
