# CDC1 - Cash Discount - Rows

- **Tabla:** CDC1
- **Descripción:** Cash Discount - Rows
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CDC1.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CdcCode` | Code | nVarChar | 20 | [OCDC](OCDC.md) |  |  |
| 2 | `LineId` | Row No. | Int | 11 | - |  |  |
| 3 | `NumOfDays` | Days | Int | 6 | - |  |  |
| 4 | `Discount` | Discount % | Num | 19.6 | - |  |  |
| 5 | `Day` | Day | Int | 6 | - |  |  |
| 6 | `Month` | Month | Int | 6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CdcCode, LineId |
