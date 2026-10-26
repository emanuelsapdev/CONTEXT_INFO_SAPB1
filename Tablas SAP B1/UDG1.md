# UDG1 - User Defaults - Documents

- **Tabla:** UDG1
- **Descripción:** User Defaults - Documents
- **Cantidad de campos:** 15
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/UDG1.html

## Campos (15)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Code | nVarChar | 8 | - |  |  |
| 2 | `ObjType` | Object Type | nVarChar | 20 | - |  |  |
| 3 | `Copies` | No. of Copies | Int | 6 | - | 1 |  |
| 4 | `PrintOnAdd` | Add & Print | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 5 | `ExprtOnAdd` | Add & Export | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `RoundSums` | Totals Rounding | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 7 | `Remark` | Permanent Remark | Text | 16 | - |  |  |
| 8 | `PrintSums` | Print Totals | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 9 | `VndrNum` | Print Mfr Catalog No. | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 10 | `PrnDscnt` | Print Discount Data | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 11 | `HandCopies` | No. of Copies for Manual Doc. | Int | 6 | - | 1 |  |
| 12 | `EngKBItem` | English Keyboard Entering Item No. | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 13 | `EngKBCard` | English Keyboard Entering BP Code | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 14 | `EmailOnAdd` | Add & E-Mail | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 15 | `PDFOnAdd` | Add & Export to PDF | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code, ObjType |
