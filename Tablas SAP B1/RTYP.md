# RTYP - Document Type List

- **Tabla:** RTYP
- **Descripción:** Document Type List
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RTYP.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CODE` | Report Type | nVarChar | 4 | - |  |  |
| 2 | `NAME` | Type Name | nVarChar | 250 | - |  |  |
| 3 | `DEFLT_REP` | Standard Report | nVarChar | 8 | - |  |  |
| 4 | `ADD_NAME` | Addon Name | nVarChar | 250 | - |  |  |
| 5 | `FRM_TYPE` | Add-On Form Type | nVarChar | 250 | - |  |  |
| 6 | `MNU_ID` | Menu Id | nVarChar | 250 | - |  |  |
| 7 | `IS_SYS` | Is sytem type or not | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 8 | `DEFLT_SEQ` | Standard Sequence | Int | 11 | - |  |  |
| 9 | `TYPE` | Type | VarChar | 1 | - | L | `L` = Layout<br>`P` = Print Sequence |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CODE |
