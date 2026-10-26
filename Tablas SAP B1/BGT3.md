# BGT3 - Budget - Cost Accounting Rows

- **Tabla:** BGT3
- **Descripción:** Budget - Cost Accounting Rows
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/BGT3.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `BudgId` | Budget Key | Int | 11 | [OBGT](OBGT.md) |  |  |
| 2 | `OcrCode` | Factor Code | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 3 | `DimCode` | In Which Dimension | Int | 6 | [ODIM](ODIM.md) |  |  |
| 4 | `Instance` | Instance | Int | 11 | [OBGS](OBGS.md) | 1 |  |
| 5 | `Line_ID` | Row Number | Int | 11 | - |  |  |
| 6 | `DebLTotal` | Monthly Budget - Deb. | Num | 19.6 | - |  |  |
| 7 | `CredLTotal` | Monthly Budget - Cr. | Num | 19.6 | - |  |  |
| 8 | `DebSTotal` | Monthly Budget - SC Deb. | Num | 19.6 | - |  |  |
| 9 | `CredSTotal` | Monthly Budget - SC Cr. | Num | 19.6 | - |  |  |
| 10 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | BudgId, OcrCode, DimCode, Line_ID |
