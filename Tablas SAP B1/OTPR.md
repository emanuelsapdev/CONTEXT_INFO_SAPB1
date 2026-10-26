# OTPR - Tax Return Values

- **Tabla:** OTPR
- **Descripción:** Tax Return Values
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OTPR.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Internal Number | Int | 11 | - |  |  |
| 2 | `Code` | Return Value Code | nVarChar | 7 | - |  |  |
| 3 | `Descr` | Description | nVarChar | 30 | - |  |  |
| 4 | `Display` | Display | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 5 | `FieldID` | Field ID in CUFD | Int | 11 | [CUFD](CUFD.md) |  |  |
| 6 | `Locked` | Locked | VarChar | 1 | - | N | `Y` = Yes<br>`N` = Changeable |
| 7 | `DataType` | Data Type | VarChar | 1 | - | S | `T` = Tax Amounts<br>`S` = Amounts<br>`P` = Prices<br>`Q` = Quantities<br>`%` = Percents<br>`I` = Integer<br>`A` = String<br>`M` = Measures |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId |
| CODE | Yes | Code |
