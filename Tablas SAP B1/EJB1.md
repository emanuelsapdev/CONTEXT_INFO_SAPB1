# EJB1 - ERV-JAb Wizard Signing Persons

- **Tabla:** EJB1
- **Descripción:** ERV-JAb Wizard Signing Persons
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/EJB1.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WizardID` | Wizard ID | Int | 11 | [OEJB](OEJB.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `Title` | Title | nVarChar | 20 | - |  |  |
| 4 | `FirstName` | First Name | nVarChar | 38 | - |  |  |
| 5 | `Surname` | Surname | nVarChar | 38 | - |  |  |
| 6 | `CommID` | Commercial ID | nVarChar | 3 | - |  |  |
| 7 | `DateOfBrth` | Date of Birth | Date | 8 | - |  |  |
| 8 | `DateOfSign` | Date of Signing | Date | 8 | - |  |  |
| 9 | `AbsEntry` | Internal Number | Int | 11 | [OEJD](OEJD.md) |  |  |
| 10 | `LineNumEJD` | Row Number EJD1 | Int | 11 | [EJD1](EJD1.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WizardID, LineNum |
