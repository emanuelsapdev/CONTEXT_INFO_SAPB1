# OFRT - Financial Report Templates

- **Tabla:** OFRT
- **Descripción:** Financial Report Templates
- **Cantidad de campos:** 15
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OFRT.html

## Campos (15)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Internal Number | Int | 11 | - |  |  |
| 2 | `Name` | Name | nVarChar | 100 | - |  |  |
| 3 | `DocType` | Template Type | VarChar | 1 | - | B | `B` = Balance Sheet<br>`P` = Profit and Loss<br>`C` = Trial Balance<br>`F` = Statement of Cash Flows<br>`S` = Sales Unit<br>`T` = Form 6111<br>`A` = Cost Accounting<br>`E` = Asset Devalue Provision<br>`R` = Shareholder's Rights and Interests Changing<br>`D` = Profit Distribution<br>`V` = VAT Payable Detail<br>`L` = e-Balance Sheet<br>`O` = e-Profit and Loss<br>`H` = Asset History Sheet<br>`G` = Others<br>`I` = Taxable Profit and Loss<br>`J` = Appropriation of Net Profit<br>`K` = E-Asset History Sheet |
| 4 | `FRTCounter` | Financial Report Template Counter | Int | 6 | - |  |  |
| 5 | `MoveChk1` | Move Chk1 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `MoveChk2` | Move Chk2 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 7 | `MoveTo_1` | Move To 1 | Int | 6 | - | 0 |  |
| 8 | `MoveTo_2` | Move To 2 | Int | 6 | - | 0 |  |
| 9 | `Title_1` | Title 1 | nVarChar | 100 | - |  |  |
| 10 | `Title_2` | Title 2 | nVarChar | 100 | - |  |  |
| 11 | `ShowMiss` | Display Missing Accounts | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 12 | `ToTitle_1` | Move To Title 1 | Int | 6 | - | 0 |  |
| 13 | `ToTitle_2` | Move To Title 2 | Int | 6 | - | 0 |  |
| 14 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 15 | `DimCode` | In Which Dimension | Int | 11 | [ODIM](ODIM.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId |
| SECOND | Yes | DocType, Name |
