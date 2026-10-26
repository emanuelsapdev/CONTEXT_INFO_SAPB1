# ATC1 - Attachments - Rows

- **Tabla:** ATC1
- **Descripción:** Attachments - Rows
- **Cantidad de campos:** 19
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ATC1.html

## Campos (19)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Absolute entry | Int | 11 | - |  |  |
| 2 | `Line` | Row Number | Int | 11 | - |  |  |
| 3 | `srcPath` | Source Path | Text | 16 | - |  |  |
| 4 | `trgtPath` | Target Path | Text | 16 | - |  |  |
| 5 | `FileName` | File Name | nVarChar | 254 | - |  |  |
| 6 | `FileExt` | File Extension | nVarChar | 8 | - |  |  |
| 7 | `Date` | Attachment Date | Date | 8 | - |  |  |
| 8 | `UsrID` | User ID | Int | 11 | - |  |  |
| 9 | `Copied` | Copied | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 10 | `Override` | Override file | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 11 | `subPath` | Subpath | nVarChar | 254 | - |  |  |
| 12 | `FreeText` | Free Text | nVarChar | 100 | - |  |  |
| 13 | `CopyToTrgt` | Copy to Target Document | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 14 | `CopyToProd` | Copy to Production Order | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 15 | `EDocSign` | EDocSign | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 16 | `SendInMail` | Send in Email | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 17 | `FileSize` | File Size | Int | 11 | - |  |  |
| 18 | `CopyFile` | Copy File | VarChar | 1 | - | N |  |
| 19 | `FileSuffix` | File suffix | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, Line |
