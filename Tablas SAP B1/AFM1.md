# AFM1 - Tax Formula Parameter Declaration

- **Tabla:** AFM1
- **Descripción:** Tax Formula Parameter Declaration
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AFM1.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `FmlId` | Formula ID | Int | 11 | [OFML](OFML.md) |  |  |
| 2 | `DispOrder` | Display Order | Int | 11 | - |  |  |
| 3 | `VarName` | Variable Name | nVarChar | 64 | - |  |  |
| 4 | `Category` | Category | VarChar | 1 | - | 1 | `1` = Input<br>`2` = Output<br>`3` = In Out |
| 5 | `Parameter` | Parameter | Text | 16 | - |  |  |
| 6 | `DataType` | Data Type | VarChar | 1 | - | S | `T` = Tax Amounts<br>`S` = Amounts<br>`P` = Prices<br>`Q` = Quantities<br>`%` = Percents<br>`I` = Integer<br>`A` = String<br>`B` = Boolean<br>`M` = Measures |
| 7 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | FmlId, DispOrder, LogInstanc |
