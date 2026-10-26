# DWZ3 - Dunning Wizard Array 3 - Recommended Service Invoice

- **Tabla:** DWZ3
- **Descripción:** Dunning Wizard Array 3 - Recommended Service Invoice
- **Cantidad de campos:** 24
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/DWZ3.html

## Campos (24)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WizardId` | Wizard ID | Int | 11 | - |  |  |
| 2 | `CardCode` | BP Card Code | nVarChar | 15 | - |  |  |
| 3 | `LetterNum` | Letter Number | Int | 11 | - |  |  |
| 4 | `AddChecked` | Add Checked | VarChar | 1 | - | Y |  |
| 5 | `DocAbs` | Internal Document Number | Int | 11 | - |  |  |
| 6 | `IntrAmt` | Interest Amount (LC) | Num | 19.6 | - |  |  |
| 7 | `IntrAmtFC` | Interest Amount (FC) | Num | 19.6 | - |  |  |
| 8 | `IntrAmtSC` | Interest Amount (SC) | Num | 19.6 | - |  |  |
| 9 | `FeeAmt` | Fee Amount (LC) | Num | 19.6 | - |  |  |
| 10 | `FeeAmtFC` | Fee Amount (FC) | Num | 19.6 | - |  |  |
| 11 | `FeeAmtSC` | Fee Amount (SC) | Num | 19.6 | - |  |  |
| 12 | `InVatGroup` | Interest VAT Group | nVarChar | 8 | - |  |  |
| 13 | `InTaxCode` | Interest Tax Code | nVarChar | 8 | - |  |  |
| 14 | `FeVatGroup` | Fee VAT Group | nVarChar | 8 | - |  |  |
| 15 | `FeTaxCode` | Fee Tax Code | nVarChar | 8 | - |  |  |
| 16 | `VatPrcnt` | VAT Percent | Num | 19.6 | - |  |  |
| 17 | `Executed` | Executed | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 18 | `Message` | Message | nVarChar | 254 | - |  |  |
| 19 | `DocCur` | Document Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 20 | `DocNum` | Document Number | Int | 11 | - |  |  |
| 21 | `BPLId` | BPL ID Assigned to Invoice | Int | 11 | - |  |  |
| 22 | `LocCode` | Location Code | Int | 11 | - |  |  |
| 23 | `SACIntrst` | SAC for Interest | Int | 11 | - |  |  |
| 24 | `SACFee` | SAC for Fee | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WizardId, CardCode, LetterNum |
