# OHLD - Holiday Table

- **Tabla:** OHLD
- **Descripción:** Holiday Table
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OHLD.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `HldCode` | Holidays Name | nVarChar | 20 | - |  |  |
| 2 | `WndFrm` | Weekend From | VarChar | 1 | - | 6 | `1` = Sunday<br>`2` = Monday<br>`3` = Tuesday<br>`4` = Wednesday<br>`5` = Thursday<br>`6` = Friday<br>`7` = Saturday |
| 3 | `WndTo` | To | VarChar | 1 | - | 1 | `1` = Sunday<br>`2` = Monday<br>`3` = Tuesday<br>`4` = Wednesday<br>`5` = Thursday<br>`6` = Friday<br>`7` = Saturday |
| 4 | `isCurYear` | Current Year | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 5 | `ignrWnd` | Ignore Weekend | VarChar | 1 | - | N |  |
| 6 | `WeekNoRule` | Rule to Calculate Week Number | VarChar | 1 | - | J | `J` = First week starts on January 1<br>`D` = First week starts in first 4-day week<br>`F` = First week starts in first full week |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | HldCode |
