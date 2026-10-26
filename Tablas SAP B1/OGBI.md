# OGBI - GB Interface: Common Info

- **Tabla:** OGBI
- **Descripción:** GB Interface: Common Info
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OGBI.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Numerator | Int | 11 | - |  |  |
| 2 | `RepNo` | Report Number | nVarChar | 20 | - |  |  |
| 3 | `RepCompany` | Report Company Name | nVarChar | 60 | - |  |  |
| 4 | `RepPeriod` | Report Period | nVarChar | 8 | - |  |  |
| 5 | `Currency` | Currency Unit | nVarChar | 10 | - |  |  |
| 6 | `UserSign` | User Signature | Int | 6 | - |  |  |
| 7 | `CreateDate` | Report Creation Date | nVarChar | 8 | - |  |  |
| 8 | `RepType` | Report Type | Int | 11 | - | 0 | `0`<br>`1` = Electronic Account Book<br>`2` = G/L Account Master Records<br>`3` = Departments<br>`16` = Employees<br>`4` = Business Partners<br>`5` = Projects<br>`6` = G/L Account Balance<br>`7` = Accounting Vouchers<br>`8` = Enterprise's Balance Sheet<br>`9` = Enterprise's Profit and Loss Statement<br>`10` = Enterprise's Cash Flow Statement<br>`11` = Devalue Provision of Enterprise Assets<br>`12` = Shareholder's Rights and Interests Changing Report<br>`13` = Enterprise's Profit Distribution Report<br>`14` = Small Enterprise's Cash Flow Statement<br>`15` = Enterprise's VAT Payable Detail Report |
| 9 | `RepEntity` | Report Entity | nVarChar | 60 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
