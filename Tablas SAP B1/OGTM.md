# OGTM - GTS Mapping Object

- **Tabla:** OGTM
- **Descripción:** GTS Mapping Object
- **Cantidad de campos:** 20
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OGTM.html

## Campos (20)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `CreateDate` | Create Date | Date | 8 | - |  |  |
| 3 | `GtsMapNum` | GTS Mapping No. | nVarChar | 20 | - |  |  |
| 4 | `InvMapEnty` | Link to Invoice Mapping ID | Int | 11 | [OIVM](OIVM.md) |  |  |
| 5 | `GtsInvNum` | Link to GTS Invoice Object | Int | 11 | [OGTI](OGTI.md) |  |  |
| 6 | `BpCode` | BP Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 7 | `BpName` | BP Name | nVarChar | 200 | - |  |  |
| 8 | `BpTaxRegNo` | BP Tax Registration No. | nVarChar | 20 | - |  |  |
| 9 | `BpAddrTel` | BP Address and Telephone | nVarChar | 80 | - |  |  |
| 10 | `BpBankNum` | BP Bank Number | nVarChar | 80 | - |  |  |
| 11 | `Remark` | Remarks | nVarChar | 254 | - |  |  |
| 12 | `Checker` | Checker | nVarChar | 80 | - |  |  |
| 13 | `Payee` | Payee | nVarChar | 80 | - |  |  |
| 14 | `DocAmount` | Document Net Amount | Num | 19.6 | - |  |  |
| 15 | `AmtAftDsct` | Amount After Discount | Num | 19.6 | - |  |  |
| 16 | `TaxAmount` | Tax Amount | Num | 19.6 | - |  |  |
| 17 | `GtsStatus` | GTS Status | VarChar | 1 | - | 1 | `1` = Exported<br>`2` = Voided<br>`3` = Imported |
| 18 | `ExportDate` | Export Date | Date | 8 | - |  |  |
| 19 | `VoidDate` | Void Date | Date | 8 | - |  |  |
| 20 | `ImportDate` | Import Date | Date | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
