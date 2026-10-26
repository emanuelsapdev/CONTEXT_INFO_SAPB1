# FTT1 - Financial Template Import - Files

- **Tabla:** FTT1
- **Descripción:** Financial Template Import - Files
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/FTT1.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [OFTT](OFTT.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `FileName` | Data Definition File Name | nVarChar | 254 | - |  |  |
| 4 | `ReleaDate` | Release Date | Date | 8 | - |  |  |
| 5 | `Descript` | Description | nVarChar | 100 | - |  |  |
| 6 | `Localizat` | Localization | nVarChar | 3 | - |  |  |
| 7 | `ChartAcct` | Chart of Accounts | nVarChar | 128 | - |  |  |
| 8 | `DocType` | Template Type | VarChar | 1 | - | B | `B` = Balance Sheet<br>`P` = Profit and Loss<br>`C` = Trial Balance<br>`F` = Statement of Cash Flows<br>`S` = Sales Unit<br>`T` = Form 6111<br>`A` = Cost Accounting<br>`E` = Asset Devalue Provision<br>`R` = Shareholder's Rights and Interests Changing<br>`D` = Profit Distribution<br>`V` = VAT Payable Detail<br>`L` = e-Balance Sheet<br>`O` = e-Profit and Loss<br>`H` = Asset History Sheet<br>`G` = Others<br>`I` = Taxable Profit and Loss<br>`J` = Appropriation of Net Profit<br>`K` = E-Asset History Sheet |
| 9 | `DimCode` | Dimension Code | Int | 11 | [ODIM](ODIM.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineNum |
