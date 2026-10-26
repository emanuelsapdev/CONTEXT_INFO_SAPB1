# IMP3 - Details and Status for Import Field

- **Tabla:** IMP3
- **Descripción:** Details and Status for Import Field
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/IMP3.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `SessionId` | Session ID | Int | 11 | - |  |  |
| 2 | `RowNumber` | RowNumber | Int | 6 | - |  |  |
| 3 | `TableName` | Table Name | nVarChar | 100 | - |  |  |
| 4 | `FileColNam` | Column Name in the Uploaded File | nVarChar | 10 | - |  |  |
| 5 | `BOFldName` | Field Name of Mapped Business Object | nVarChar | 50 | - |  |  |
| 6 | `BOFldDesc` | Descriptive Field Name of Mapped Business Object | nVarChar | 100 | - |  |  |
| 7 | `FieldValue` | Field Value | nVarChar | 100 | - |  |  |
| 8 | `Validation` | Validation Method | VarChar | 1 | - |  | `D` = Fill with Default Values<br>`C` = Clean Data<br>`M` = Validate with Metadata<br>`V` = Custom Validation |
| 9 | `ValidRes` | Validation Result | VarChar | 1 | - |  | `N` = Not Validated<br>`Y` = Validation Successful<br>`E` = Error in Validation |
| 10 | `ValidMsg` | Validation Message | nVarChar | 100 | - |  |  |
| 11 | `Line_ID` | Line Number | Int | 11 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | SessionId, RowNumber, Line_ID |
