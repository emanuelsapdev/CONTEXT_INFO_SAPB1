# MSN2 - MRP Run Results

- **Tabla:** MSN2
- **Descripción:** MRP Run Results
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MSN2.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 3 | `PeriodID` | Period ID | Int | 11 | - |  |  |
| 4 | `Initial` | Initial Quantity | Num | 19.6 | - |  |  |
| 5 | `InitialOrg` | Original Initial Quantity | Num | 19.6 | - |  |  |
| 6 | `InStock` | Incoming Stock | Num | 19.6 | - |  |  |
| 7 | `OutStock` | Outgoing Stock | Num | 19.6 | - |  |  |
| 8 | `Final` | Final Quantity | Num | 19.6 | - |  |  |
| 9 | `FinalOrg` | Original Final Quantity | Num | 19.6 | - |  |  |
| 10 | `Requests` | Requests | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, PeriodID, ItemCode |
