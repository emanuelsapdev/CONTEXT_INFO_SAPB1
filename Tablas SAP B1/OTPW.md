# OTPW - Tax Payment Wizard

- **Tabla:** OTPW
- **Descripción:** Tax Payment Wizard
- **Cantidad de campos:** 17
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OTPW.html

## Campos (17)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | - |  |  |
| 2 | `WizNumber` | Wizard Number | Int | 11 | - |  |  |
| 3 | `WizName` | Wizard Name | nVarChar | 50 | - |  |  |
| 4 | `WizStatus` | Wizard Status | VarChar | 1 | - | S | `S` = Saved<br>`E` = Executed |
| 5 | `CreateDate` | Wizard Creation Date | Date | 8 | - |  |  |
| 6 | `SaveDate` | Wizard Save Date | Date | 8 | - |  |  |
| 7 | `ExecDate` | Wizard Execution Date | Date | 8 | - |  |  |
| 8 | `UserSign` | User Signature | Int | 6 | - |  |  |
| 9 | `Series` | Wizard Series | Int | 11 | - |  |  |
| 10 | `JETransId` | Journal Entry Number | Int | 11 | [OJDT](OJDT.md) |  |  |
| 11 | `WizDate` | Wizard Date | Date | 8 | - |  |  |
| 12 | `RG23APart2` | RG23A Part 2 | Int | 11 | - |  |  |
| 13 | `RG23CPart2` | RG23C Part 2 | Int | 11 | - |  |  |
| 14 | `SeqCode` | Sequence Code | Int | 6 | - |  |  |
| 15 | `Serial` | Serial Number | Int | 11 | - |  |  |
| 16 | `SeriesStr` | Series String | nVarChar | 3 | - |  |  |
| 17 | `SubStr` | Subseries String | nVarChar | 3 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| NAME | Yes | WizName |
