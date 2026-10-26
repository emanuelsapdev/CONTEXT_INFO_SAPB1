# VPM4 - Outgoing Payments - Accounts

- **Tabla:** VPM4
- **Descripción:** Outgoing Payments - Accounts
- **Cantidad de campos:** 36
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/VPM4.html

## Campos (36)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocNum` | Document Number | Int | 11 | [OVPM](OVPM.md) |  |  |
| 2 | `LineId` | Row Number | Int | 11 | - |  |  |
| 3 | `AcctCode` | Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 4 | `SumApplied` | Paid | Num | 19.6 | - |  |  |
| 5 | `AppliedFC` | Paid in FC | Num | 19.6 | - |  |  |
| 6 | `AppliedSys` | Paid in SC | Num | 19.6 | - |  |  |
| 7 | `Descrip` | Description | nVarChar | 250 | - |  |  |
| 8 | `VatGroup` | VAT Group | nVarChar | 8 | [OVTG](OVTG.md) |  |  |
| 9 | `VatPrcnt` | VAT Rate | Num | 19.6 | - |  |  |
| 10 | `AcctName` | Account Name | nVarChar | 200 | - |  |  |
| 11 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 46 |  |
| 12 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 13 | `OcrCode` | Distribution Rule | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 14 | `Project` | Project Code | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 15 | `GrossAmnt` | Gross Amount | Num | 19.6 | - |  |  |
| 16 | `GrssAmntFC` | Gross Amount (FC) | Num | 19.6 | - |  |  |
| 17 | `GrssAmntSC` | Gross Amount (SC) | Num | 19.6 | - |  |  |
| 18 | `AmntBase` | Base Amount | VarChar | 1 | - |  | `E` = Exclude Tax<br>`I` = Include Tax |
| 19 | `VatAmnt` | VAT Amount | Num | 19.6 | - |  |  |
| 20 | `VatAmntFC` | VAT Amount (FC) | Num | 19.6 | - |  |  |
| 21 | `VatAmntSC` | VAT Amount (SC) | Num | 19.6 | - |  |  |
| 22 | `UserChaVat` | User Changed VAT | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 23 | `TaxTypeID` | Tax Type Component ID | Int | 11 | [OSTT](OSTT.md) |  |  |
| 24 | `OcrCode2` | Distribution Rule2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 25 | `OcrCode3` | Distribution Rule3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 26 | `OcrCode4` | Distribution Rule4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 27 | `OcrCode5` | Distribution Rule5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 28 | `Section` | Section | Int | 11 | [OSEC](OSEC.md) |  |  |
| 29 | `AsseType` | Assessee Type | VarChar | 1 | - |  | `C` = Company<br>`P` = Others |
| 30 | `LocCode` | Location Code | Int | 11 | [OLCT](OLCT.md) |  |  |
| 31 | `MatType` | Material Type | Int | 11 | - | 0 |  |
| 32 | `EquVatPer` | Equalization Tax Rate | Num | 19.6 | - |  |  |
| 33 | `EquVatSum` | Equalization VAT Amount | Num | 19.6 | - |  |  |
| 34 | `EquVatSumF` | Equalization VAT Amount (FC) | Num | 19.6 | - |  |  |
| 35 | `EquVatSumS` | Equalization VAT Amount (SC) | Num | 19.6 | - |  |  |
| 36 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocNum, LineId |
