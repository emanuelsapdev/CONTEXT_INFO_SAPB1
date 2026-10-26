# OQCN - Query Catagories

- **Tabla:** OQCN
- **Descripción:** Query Catagories
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OQCN.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CategoryId` | Category ID | Int | 11 | - |  |  |
| 2 | `CatName` | Category Name | nVarChar | 50 | - |  |  |
| 3 | `PermMask` | Permissions | nVarChar | 20 | - | NNNNNNNNNNNNNNN |  |
| 4 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Upgrade<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 5 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CategoryId |
| CAT_NAME_K | No | CatName |
