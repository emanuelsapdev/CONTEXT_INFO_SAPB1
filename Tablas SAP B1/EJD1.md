# EJD1 - ERV-JAb Signing Persons List

- **Tabla:** EJD1
- **Descripción:** ERV-JAb Signing Persons List
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/EJD1.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [OEJD](OEJD.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `Title` | Title | nVarChar | 20 | - |  |  |
| 4 | `FirstName` | First Name | nVarChar | 38 | - |  |  |
| 5 | `Surname` | Surname | nVarChar | 38 | - |  |  |
| 6 | `CommID` | Commercial ID | nVarChar | 3 | - |  |  |
| 7 | `DateOfBrth` | Date of Birth | Date | 8 | - |  |  |
| 8 | `Active` | Active | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineNum |
