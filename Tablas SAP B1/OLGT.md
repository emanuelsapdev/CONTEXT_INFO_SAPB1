# OLGT - Length Units

- **Tabla:** OLGT
- **Descripción:** Length Units
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OLGT.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `UnitCode` | Unit Code | Int | 6 | - |  |  |
| 2 | `UnitDisply` | Unit Display | nVarChar | 2 | - |  |  |
| 3 | `UnitName` | Unit Name | nVarChar | 20 | - |  |  |
| 4 | `VolDisply` | Unit Code for Quantity Display | nVarChar | 3 | - |  |  |
| 5 | `SizeInMM` | Unit Length in mm | Num | 19.6 | - |  |  |
| 6 | `Locked` | Locked | VarChar | 1 | - | N | `N` = Changeable<br>`Y` = Locked |
| 7 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 8 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (4)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | UnitCode |
| DISPLAY | Yes | UnitDisply |
| UNIT_NAME | Yes | UnitName |
| VOLUME | No | VolDisply |
