# OFRM - File Format

- **Tabla:** OFRM
- **Descripción:** File Format
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OFRM.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `Name` | File Format Name | nVarChar | 100 | - |  |  |
| 3 | `Encoding` | Encoding Type | nVarChar | 100 | - |  |  |
| 4 | `FilePath` | Format Project | Text | 16 | - |  |  |
| 5 | `IsSystem` | System Format | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `FrmatType` | Format Type | VarChar | 1 | - | O | `I` = Bank Statements<br>`O` = Payment File<br>`L` = Legal List<br>`P` = Predefined<br>`B` = Boleto File<br>`R` = Padron File |
| 7 | `FileContnt` | Format Project Content | Text | 16 | - |  |  |
| 8 | `FrmatStats` | Format Status | VarChar | 1 | - | U | `A` = Assigned<br>`U` = Unassigned |
| 9 | `PaymType` | Payment Type | VarChar | 1 | - | X | `O` = Outgoing<br>`I` = Incoming<br>`X` |
| 10 | `Hash` | Binary Content Hash | nVarChar | 128 | - |  |  |
| 11 | `FileName` | File Name | Text | 16 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| NAME_TYPE | No | Name, FrmatType |
