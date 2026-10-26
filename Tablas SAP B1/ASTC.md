# ASTC - Sales Tax Codes

- **Tabla:** ASTC
- **Descripción:** Sales Tax Codes
- **Cantidad de campos:** 23
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ASTC.html

## Campos (23)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Code | nVarChar | 8 | - |  |  |
| 2 | `Name` | Name | nVarChar | 100 | - |  |  |
| 3 | `Rate` | Rate | Num | 19.6 | - |  |  |
| 4 | `Freight` | Freight | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 5 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 6 | `ValidForAR` | Valid for A/R | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 7 | `ValidForAP` | Valid for A/P | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 8 | `TfcId` | Formula Combination ID | Int | 11 | [OTFC](OTFC.md) |  |  |
| 9 | `Lock` | Inactive | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 10 | `TaxIcms` | Taxation For ICMS | nVarChar | 2 | - |  |  |
| 11 | `IsItmLevel` | Single Item Level Tax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 12 | `CfopIn` | CFOP Incoming Code | nVarChar | 6 | [OCFP](OCFP.md) |  |  |
| 13 | `CfopOut` | CFOP Outgoing Code | nVarChar | 6 | [OCFP](OCFP.md) |  |  |
| 14 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 15 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 16 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 17 | `FADebit` | FA Debit | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 18 | `IsSystem` | Is System Tax Code | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 19 | `VatExempt` | Apply VAT Exemption | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 20 | `HashInpNm` | Hash Input Name | nVarChar | 100 | - |  |  |
| 21 | `CheckDate` | Check Date | Date | 8 | - |  |  |
| 22 | `EfctDate` | Effective From | Date | 8 | - |  |  |
| 23 | `Provider` | Tax Service Provider | nVarChar | 50 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code, LogInstanc |
