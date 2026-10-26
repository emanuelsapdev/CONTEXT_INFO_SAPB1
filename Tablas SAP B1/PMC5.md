# PMC5 - Project Management Configuration - Activity Type

- **Tabla:** PMC5
- **Descripción:** Project Management Configuration - Activity Type
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/PMC5.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ActTypeID` | Activity Type No. | Int | 11 | - |  |  |
| 2 | `ActType` | Activity Type | nVarChar | 100 | - |  |  |
| 3 | `LaborItem` | Labor Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 4 | `Chargeable` | Chargeable | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 5 | `Absence` | Absence | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 6 | `AbsenceID` | Absence No. | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ActTypeID |
