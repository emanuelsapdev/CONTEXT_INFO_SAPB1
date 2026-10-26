# BGT2 - Budget - Cost Accounting

- **Tabla:** BGT2
- **Descripción:** Budget - Cost Accounting
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/BGT2.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `BudgId` | Budget Key | Int | 11 | [OBGT](OBGT.md) |  |  |
| 2 | `OcrCode` | Factor Code | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 3 | `DimCode` | In Which Dimension | Int | 6 | [ODIM](ODIM.md) |  |  |
| 4 | `Instance` | Instance | Int | 11 | [OBGS](OBGS.md) | 1 |  |
| 5 | `DebLTotal` | Tot. Annu. Budgt Debit (LC) | Num | 19.6 | - |  |  |
| 6 | `CredLTotal` | Tot. Annu. Budgt Credit (LC) | Num | 19.6 | - |  |  |
| 7 | `DebSTotal` | Tot. Annu. Budgt Debit (SC) | Num | 19.6 | - |  |  |
| 8 | `CredSTotal` | Tot. Annu. Budgt Credit (SC) | Num | 19.6 | - |  |  |
| 9 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | BudgId, OcrCode, DimCode |
