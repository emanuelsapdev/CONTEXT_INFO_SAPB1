# GPA8 - Product Cost Adjustment - MRV Document Lines

- **Tabla:** GPA8
- **Descripción:** Product Cost Adjustment - MRV Document Lines
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/GPA8.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | [OGPA](OGPA.md) |  |  |
| 2 | `LineId` | Row No. | Int | 11 | - |  |  |
| 3 | `ProdCode` | Product Code | nVarChar | 20 | - |  |  |
| 4 | `ProdDescr` | Product Description | nVarChar | 200 | - |  |  |
| 5 | `DistNumber` | Batch Number | nVarChar | 36 | - |  |  |
| 6 | `SnBAbs` | SnB Abs. Entry | Int | 11 | - |  |  |
| 7 | `ManagedBy` | Managed By | Int | 11 | - | -1 | `10000044` = Batch Numbers<br>`10000045` = Serial Numbers<br>`-1` |
| 8 | `IncrAcct` | G/L Increase Account | nVarChar | 15 | - |  |  |
| 9 | `DecrAcct` | G/L Decrease Account | nVarChar | 15 | - |  |  |
| 10 | `DebCredAmt` | Debit/Credit Amount | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineId |
