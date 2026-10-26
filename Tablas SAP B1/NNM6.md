# NNM6 - Documents Numbering - Supplementary Code

- **Tabla:** NNM6
- **Descripción:** Documents Numbering - Supplementary Code
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/NNM6.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ObjectCode` | Document | nVarChar | 20 | [ONNM](ONNM.md) |  |  |
| 2 | `PeriodType` | Sequence Period Type | VarChar | 1 | - |  | `Y` = Annually<br>`M` = Monthly<br>`W` = Weekly<br>`P` = Permanent |
| 3 | `StartDate` | Start Date | Date | 8 | - |  |  |
| 4 | `EndDate` | End Date | Date | 8 | - |  |  |
| 5 | `Sequence` | Current Sequence | Int | 11 | - |  |  |
| 6 | `FormatStr` | Format String for Create Code | nVarChar | 254 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ObjectCode, PeriodType, StartDate, EndDate |
