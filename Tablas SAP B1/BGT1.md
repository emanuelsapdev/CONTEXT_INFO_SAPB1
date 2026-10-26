# BGT1 - Budget - Rows

- **Tabla:** BGT1
- **Descripción:** Budget - Rows
- **Cantidad de campos:** 23
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/BGT1.html

## Campos (23)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `BudgId` | Budget Key | Int | 11 | [OBGT](OBGT.md) |  |  |
| 2 | `Line_ID` | Row Number | Int | 11 | - | 0 |  |
| 3 | `DebLTotal` | Monthly Budget - Deb. | Num | 19.6 | - |  |  |
| 4 | `CredLTotal` | Monthly Budget - Cr. | Num | 19.6 | - |  |  |
| 5 | `DebSTotal` | Monthly Budget - SC Deb. | Num | 19.6 | - |  |  |
| 6 | `CredSTotal` | Monthly Budget - SC Cr. | Num | 19.6 | - |  |  |
| 7 | `DebRLTotal` | Monthly Bal. - Deb. | Num | 19.6 | - |  |  |
| 8 | `CrdRLTotal` | Monthly Bal. - Cr. | Num | 19.6 | - |  |  |
| 9 | `DebRSTotal` | Monthly Bal. - SC Deb. | Num | 19.6 | - |  |  |
| 10 | `CrdRSTotal` | Monthly Bal. - SC Cred. | Num | 19.6 | - |  |  |
| 11 | `FtrIDRLSum` | Fut. Monthly Incomes SC Cr. | Num | 19.6 | - |  |  |
| 12 | `FtrIDRSSum` | Fut. Monthly Incomes SC Deb. | Num | 19.6 | - |  |  |
| 13 | `FtrICRLSum` | Fut. Incomes - Cr. | Num | 19.6 | - |  |  |
| 14 | `FtrICRSSum` | Fut. Incomes - Sys. Cr. | Num | 19.6 | - |  |  |
| 15 | `FtrODRLSum` | Fut. Expen - Local Deb. | Num | 19.6 | - |  |  |
| 16 | `FtrODRSSum` | Fut.Expen - SC Deb. | Num | 19.6 | - |  |  |
| 17 | `FtrOCRLSum` | Fut.Expen - Local Cr. | Num | 19.6 | - |  |  |
| 18 | `FtrOCRSSum` | Fut.Expen - Sys. Cr. | Num | 19.6 | - |  |  |
| 19 | `MonthPrcnt` | % of annual budget amount | Num | 19.6 | - |  |  |
| 20 | `LineMemo` | Row Details | nVarChar | 50 | - |  |  |
| 21 | `Instance` | Instance | Int | 11 | [OBGS](OBGS.md) | 1 |  |
| 22 | `AcctCode` | Account Code | nVarChar | 15 | - |  |  |
| 23 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | BudgId, Line_ID |
