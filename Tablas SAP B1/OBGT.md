# OBGT - Budget

- **Tabla:** OBGT
- **Descripción:** Budget
- **Cantidad de campos:** 25
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OBGT.html

## Campos (25)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Internal Number | Int | 11 | - |  |  |
| 2 | `AcctCode` | Account Code | nVarChar | 15 | - |  |  |
| 3 | `BgdCode` | Division Code | Int | 11 | [OBGD](OBGD.md) |  |  |
| 4 | `FatherCode` | Parent Account Key | nVarChar | 15 | - |  |  |
| 5 | `FthrPrcnt` | Parent Acct % | Num | 19.6 | - |  |  |
| 6 | `DebLTotal` | Total Annual Budget - Debit (LC) | Num | 19.6 | - |  |  |
| 7 | `CredLTotal` | Total Annual Budget - Credit (LC) | Num | 19.6 | - |  |  |
| 8 | `DebSTotal` | Total Annual Budget - Debit (SC) | Num | 19.6 | - |  |  |
| 9 | `CredSTotal` | Total Annual Budget - Credit (SC) | Num | 19.6 | - |  |  |
| 10 | `DebRLTotal` | Budget Balance - Debit (LC) | Num | 19.6 | - |  |  |
| 11 | `CrdRLTotal` | Budget Balance - Credit (LC) | Num | 19.6 | - |  |  |
| 12 | `DebRSTotal` | Budget Balance - Debit (SC) | Num | 19.6 | - |  |  |
| 13 | `CrdRSTotal` | Budget Balance - Credit (SC) | Num | 19.6 | - |  |  |
| 14 | `FtrIDRLSum` | Future Annual Revenues - Debit (LC) | Num | 19.6 | - |  |  |
| 15 | `FtrIDRSSum` | Future Annual Revenues - Credit (SC) | Num | 19.6 | - |  |  |
| 16 | `FtrICRLSum` | Future Revenues - Debit (LC) | Num | 19.6 | - |  |  |
| 17 | `FtrICRSSum` | Future Revenues - Debit (SC) | Num | 19.6 | - |  |  |
| 18 | `FtrODRLSum` | Future Annual Expenses - Credit (LC) | Num | 19.6 | - |  |  |
| 19 | `FtrOCRLSum` | Future Annual Expenses - Debit (LC) | Num | 19.6 | - |  |  |
| 20 | `FtrODRSSum` | Future Annual Expenses - Credit (SC) | Num | 19.6 | - |  |  |
| 21 | `FtrOCRSSum` | Future Annual Expenses - Debit (SC) | Num | 19.6 | - |  |  |
| 22 | `FinancYear` | Start of Fiscal Year | Date | 8 | - |  |  |
| 23 | `Instance` | Instance | Int | 11 | [OBGS](OBGS.md) | 1 |  |
| 24 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 25 | `SCNCounter` | SCN Counter | Int | 6 | - |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId |
| ACCNT_CODE | Yes | AcctCode, FinancYear, Instance |
| INTER_KEY | No | FatherCode |
