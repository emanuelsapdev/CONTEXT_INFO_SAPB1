# OFNS - Folio Numbering - Series

- **Tabla:** OFNS
- **Descripción:** Folio Numbering - Series
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OFNS.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Series` | Series ID | Int | 11 | - |  |  |
| 2 | `Name` | Name | nVarChar | 100 | - |  |  |
| 3 | `PTICode` | POI Code | nVarChar | 5 | [OPTI](OPTI.md) |  |  |
| 4 | `FirstNum` | First Number | Int | 11 | - |  |  |
| 5 | `NextNum` | Next Number | Int | 11 | - |  |  |
| 6 | `LastNum` | Last Number | Int | 11 | - |  |  |
| 7 | `Letter` | Letter | VarChar | 1 | - |  | `A` = A<br>`B` = B<br>`C` = C<br>`E` = E<br>`M` = M<br>`R` = R<br>`T` = T<br>`X` = X<br>`-` = - |
| 8 | `CAI` | CAI | nVarChar | 14 | - |  |  |
| 9 | `CAIDueDate` | CAI Due Date | Date | 8 | - |  |  |
| 10 | `Remarks` | Remarks | nVarChar | 100 | - |  |  |
| 11 | `Locked` | Locked | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Series |
| NAME | Yes | Name |
