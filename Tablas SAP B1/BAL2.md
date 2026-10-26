# BAL2 - Period indicators for opening Balance

- **Tabla:** BAL2
- **Descripción:** Period indicators for opening Balance
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/BAL2.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `PeriodID` | Period Indicator | Int | 11 | - |  |  |
| 2 | `DateFrom` | Date From | Date | 8 | - |  |  |
| 3 | `DateTo` | Date To | Date | 8 | - |  |  |
| 4 | `FiscalYear` | Fiscal Year | Int | 11 | - |  |  |
| 5 | `CreateDate` | Create Date | Date | 8 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | PeriodID |
| SECONDARY | Yes | DateFrom, DateTo |
