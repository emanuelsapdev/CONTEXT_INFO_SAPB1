# WTC1 - WTax Certificates - WT Groups in Certificates

- **Tabla:** WTC1
- **Descripción:** WTax Certificates - WT Groups in Certificates
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WTC1.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `LineId` | Row Number | Int | 11 | - |  |  |
| 3 | `WtAbsEntry` | Internal Number | Int | 11 | - |  |  |
| 4 | `WTPercent` | WTax Rate | Num | 19.6 | - |  |  |
| 5 | `SumVatAmnt` | Sum of VAT Amount | Num | 19.6 | - |  |  |
| 6 | `SumDocTot` | Sum of Doc. Total Amount | Num | 19.6 | - |  |  |
| 7 | `SumBaseAmn` | Sum of Base Amount | Num | 19.6 | - |  |  |
| 8 | `SumAccumAm` | Sum of Accumulated Amount | Num | 19.6 | - |  |  |
| 9 | `SumPercpAm` | Sum of Perception Amount | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineId |
