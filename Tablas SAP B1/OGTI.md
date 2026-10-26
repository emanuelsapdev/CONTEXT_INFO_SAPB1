# OGTI - GTS Invoice

- **Tabla:** OGTI
- **Descripción:** GTS Invoice
- **Cantidad de campos:** 26
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OGTI.html

## Campos (26)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `CreateDate` | Create Date | Date | 8 | - |  |  |
| 3 | `MappingNum` | GTS Mapping No. | nVarChar | 20 | - |  |  |
| 4 | `Voiding` | Voiding Flag | VarChar | 1 | - | 0 | `0` = Normal<br>`1` = Voided |
| 5 | `ItemList` | Item List | VarChar | 1 | - |  | `0` = Without Item List<br>`1` = With Item List |
| 6 | `CategNum` | GTS Cat. No. | nVarChar | 20 | - |  |  |
| 7 | `GtsInvNum` | GTS Invoice No. | nVarChar | 30 | - |  |  |
| 8 | `ItemRowNum` | Item List Row Number | Int | 11 | - |  |  |
| 9 | `DocDate` | Document Date | Date | 8 | - |  |  |
| 10 | `FiscaMonth` | Fiscal Month | Int | 6 | - |  |  |
| 11 | `DocAmount` | Document Amount | Num | 19.6 | - |  |  |
| 12 | `VatPercent` | VAT Percent | Num | 19.6 | - |  |  |
| 13 | `VatAmount` | VAT Amount | Num | 19.6 | - |  |  |
| 14 | `BpName` | BP Name | nVarChar | 200 | - |  |  |
| 15 | `BpTaxRgNum` | BP Tax Registration No. | nVarChar | 20 | - |  |  |
| 16 | `BpAddrTel` | BP Address and Telephone | nVarChar | 80 | - |  |  |
| 17 | `BpBankNum` | BP Bank Number | nVarChar | 60 | - |  |  |
| 18 | `SellerName` | Seller Name | nVarChar | 80 | - |  |  |
| 19 | `SelTaxReg` | Seller Tax Registration No. | nVarChar | 80 | - |  |  |
| 20 | `SelAddTel` | Seller Address and Tel. | nVarChar | 80 | - |  |  |
| 21 | `SelBankAct` | Seller Bank Account | nVarChar | 80 | - |  |  |
| 22 | `Remarks` | Remarks | nVarChar | 160 | - |  |  |
| 23 | `Issuer` | Issuer | nVarChar | 8 | - |  |  |
| 24 | `Checker` | Checker | nVarChar | 8 | - |  |  |
| 25 | `Payee` | Payee | nVarChar | 8 | - |  |  |
| 26 | `InBndFile` | Inbound File: Full Name | nVarChar | 254 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
