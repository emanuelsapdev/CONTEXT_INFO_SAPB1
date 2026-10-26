# TYPR - TYPR

- **Tabla:** TYPR
- **Descripción:** TYPR
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TYPR.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CODE` | Report Type | nVarChar | 4 | - |  |  |
| 2 | `NAME` | Type Name | nVarChar | 250 | - |  |  |
| 3 | `DEFLT_REP` | Standard Report | nVarChar | 8 | - |  |  |
| 4 | `Local` | Localization | nVarChar | 2 | - |  |  |
| 5 | `Created` | Creation Date | Date | 8 | - |  |  |
| 6 | `Updated` | Updated Date | Date | 8 | - |  |  |
| 7 | `UsrSgnStr` | User Sign For Strings Change | Int | 11 | - | -1 |  |
| 8 | `ResCode` | Resource Code from RSBD | Int | 11 | - | -1 |  |
| 9 | `RevCode` | Revision Code | Int | 11 | - | -1 |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CODE, Local, ResCode, RevCode |
| TYPE | No | CODE |
