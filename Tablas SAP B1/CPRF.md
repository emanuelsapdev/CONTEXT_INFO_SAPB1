# CPRF - Column Preferences

- **Tabla:** CPRF
- **Descripción:** Column Preferences
- **Cantidad de campos:** 17
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CPRF.html

## Campos (17)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `FormID` | Form ID | nVarChar | 20 | - |  |  |
| 2 | `ItemID` | Item Number | nVarChar | 50 | - |  |  |
| 3 | `ColID` | Column | nVarChar | 60 | - |  |  |
| 4 | `Width` | Width | Int | 11 | - |  |  |
| 5 | `VisInForm` | Visible in Form | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `VisualIndx` | Tabs Layout | Int | 11 | - |  |  |
| 7 | `EditInForm` | Editable in Form | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `VisInExpnd` | Visible in Expanded | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 9 | `ExpandIndx` | Expanded Index | Int | 11 | - |  |  |
| 10 | `EditInEXP` | Editable in Expanded | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 11 | `Folded` | Folder | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 12 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 13 | `ExtDisable` | Externally Disabled | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 14 | `ExtInvsbl` | Externally Invisible | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 15 | `TPLId` | Template ID | Int | 6 | [UICU](UICU.md) | 0 |  |
| 16 | `TableName` | Table Name | nVarChar | 20 | - |  |  |
| 17 | `ItemUID` | ItemUID | nVarChar | 32 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | UserSign, FormID, ItemID, ColID, TPLId |
