# OWGT - Weight Units

- **Tabla:** OWGT
- **Descripción:** Weight Units
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OWGT.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `UnitCode` | Unit Code | Int | 6 | - |  |  |
| 2 | `UnitDisply` | Code | nVarChar | 2 | - |  |  |
| 3 | `UnitName` | Unit Name | nVarChar | 20 | - |  |  |
| 4 | `WightInMG` | Weight (mg) | Num | 19.6 | - |  |  |
| 5 | `Locked` | Locked | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 7 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | UnitCode |
| DISPLAY | Yes | UnitDisply |
| UNIT_NAME | Yes | UnitName |
