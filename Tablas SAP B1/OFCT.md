# OFCT - Sales Forecast

- **Tabla:** OFCT
- **Descripción:** Sales Forecast
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OFCT.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsID` | Internal Number | Int | 11 | - |  |  |
| 2 | `Code` | Forecast Code | nVarChar | 16 | - |  |  |
| 3 | `Name` | Forecast Name | nVarChar | 100 | - |  |  |
| 4 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 5 | `StartDate` | Forecast Start Date | Date | 8 | - |  |  |
| 6 | `EndDate` | Forecast End Date | Date | 8 | - |  |  |
| 7 | `FormView` | Forecast Form View | VarChar | 1 | - | D | `D` = Daily<br>`W` = Weekly<br>`M` = Monthly |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsID |
| FCT_CODE | Yes | Code |
