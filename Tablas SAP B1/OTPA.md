# OTPA - Tax Parameter Attributes

- **Tabla:** OTPA
- **Descripción:** Tax Parameter Attributes
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OTPA.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Internal Number | Int | 11 | - |  |  |
| 2 | `Code` | Attribute Code | nVarChar | 8 | - |  |  |
| 3 | `Descr` | Description | nVarChar | 30 | - |  |  |
| 4 | `DataType` | Data Type | VarChar | 1 | - | S | `S` = Amounts<br>`P` = Prices<br>`Q` = Quantities<br>`%` = Percents<br>`I` = Integer<br>`A` = String<br>`M` = Measures |
| 5 | `FieldId` | Field ID in CUFD | Int | 11 | [CUFD](CUFD.md) |  |  |
| 6 | `Locked` | Locked | VarChar | 1 | - | N | `Y` = Yes<br>`N` = Changeable |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId |
| CODE | Yes | Code |
