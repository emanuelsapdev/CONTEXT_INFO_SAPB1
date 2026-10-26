# FLT1 - 856 Report - Selection Criteria

- **Tabla:** FLT1
- **Descripción:** 856 Report - Selection Criteria
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/FLT1.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `FormNo` | Form No. | nVarChar | 20 | - |  |  |
| 2 | `Code` | Code | nVarChar | 50 | - |  |  |
| 3 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 4 | `ExNumData1` | Extra Numeric Data 1 | Int | 11 | - |  |  |
| 5 | `ExNumData2` | Extra Numeric Data 2 | Int | 11 | - |  |  |
| 6 | `ExNumData3` | Extra Numeric Data 3 | Int | 11 | - |  |  |
| 7 | `ExStrData1` | Extra String Data 1 | nVarChar | 254 | - |  |  |
| 8 | `ExStrData2` | Extra String Data 2 | nVarChar | 254 | - |  |  |
| 9 | `ExStrData3` | Extra String Data 3 | nVarChar | 254 | - |  |  |
| 10 | `FilterName` | Filter Name | nVarChar | 30 | - | _ |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | FormNo, UserSign, Code, FilterName |
