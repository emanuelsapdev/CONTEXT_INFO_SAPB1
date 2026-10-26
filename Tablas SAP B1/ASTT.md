# ASTT - Sales Tax Authorities Type

- **Tabla:** ASTT
- **Descripción:** Sales Tax Authorities Type
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ASTT.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Numerator | Int | 11 | - |  |  |
| 2 | `Name` | Type Name | nVarChar | 40 | - |  |  |
| 3 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 4 | `IsVat` | VAT | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 5 | `NfTaxId` | ID of Nota Fiscal Tax Category | Int | 11 | [ONFT](ONFT.md) |  |  |
| 6 | `TpsId` | ID of Tax Parameter Set | Int | 11 | [OTPS](OTPS.md) |  |  |
| 7 | `PLABalance` | PLA Current Balance | Num | 19.6 | - |  |  |
| 8 | `Locked` | Locked | VarChar | 1 | - | N |  |
| 9 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 10 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 11 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 12 | `CreditCtrl` | Tax Credit Control | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId, LogInstanc |
| NAME | Yes | Name, LogInstanc |
