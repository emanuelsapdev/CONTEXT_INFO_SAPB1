# OCDP - Closing Date Procedure

- **Tabla:** OCDP
- **Descripción:** Closing Date Procedure
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCDP.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ClsDateNum` | Closing Date Procedure Number | Int | 6 | - |  |  |
| 2 | `ClsDtCode` | Closing Date Procedure Code | nVarChar | 30 | - |  |  |
| 3 | `BsLineDate` | Base Row Date | VarChar | 1 | - | S | `P` = Posting Date<br>`S` = System Date |
| 4 | `DueMonth` | Start From | VarChar | 1 | - | N | `E` = Month End<br>`H` = Half Month<br>`Y` = Month Start<br>`N` |
| 5 | `ExtraMonth` | Extra Month | Int | 6 | - |  |  |
| 6 | `ExtraDay` | Extra Day | Int | 6 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ClsDateNum |
| ABS_ENTRY | Yes | ClsDtCode |
