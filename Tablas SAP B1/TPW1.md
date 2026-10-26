# TPW1 - Selection Criteria

- **Tabla:** TPW1
- **Descripción:** Selection Criteria
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TPW1.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Absolute Entry No | Int | 11 | [OTPW](OTPW.md) |  |  |
| 2 | `FromPeriod` | From Period | Date | 8 | - |  |  |
| 3 | `ToPeriod` | To Period | Date | 8 | - |  |  |
| 4 | `FromDate` | From Date | Date | 8 | - |  |  |
| 5 | `ToDate` | To Date | Date | 8 | - |  |  |
| 6 | `TaxCategry` | Tax Category | Int | 11 | [ONFT](ONFT.md) |  |  |
| 7 | `LocCode` | Location Code | Int | 11 | [OLCT](OLCT.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
