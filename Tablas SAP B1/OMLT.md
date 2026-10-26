# OMLT - Multi-Language Translation

- **Tabla:** OMLT
- **Descripción:** Multi-Language Translation
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OMLT.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TranEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `TableName` | Table Name | nVarChar | 20 | - |  |  |
| 3 | `FieldAlias` | Field Alias | nVarChar | 50 | - |  |  |
| 4 | `PK` | Primary Key of Object | nVarChar | 254 | - |  |  |
| 5 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Upgrade<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 6 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TranEntry |
| Second | Yes | TableName, FieldAlias, PK |
