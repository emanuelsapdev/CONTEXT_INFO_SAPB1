# OJET - JE Document Type

- **Tabla:** OJET
- **Descripción:** JE Document Type
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OJET.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `JEType` | JE Document Type | nVarChar | 60 | - |  |  |
| 2 | `Locked` | Locked | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 3 | `DocTypDesc` | Document Type Description | nVarChar | 254 | - |  |  |
| 4 | `ShortName` | Short Name | nVarChar | 254 | - |  |  |
| 5 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 6 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | JEType |
