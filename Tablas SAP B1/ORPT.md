# ORPT - Response Type

- **Tabla:** ORPT
- **Descripción:** Response Type
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ORPT.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Dscrptn` | Response Description | nVarChar | 100 | - |  |  |
| 2 | `RspType` | Response Type | nVarChar | 20 | - |  |  |
| 3 | `IsActived` | Active | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | RspType |
