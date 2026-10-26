# OCLQ - Questions for "Ask AI" App in Web Client

- **Tabla:** OCLQ
- **Descripción:** Questions for "Ask AI" App in Web Client
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCLQ.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Id` | Internal Question ID | Int | 11 | - |  |  |
| 2 | `Name` | Question Title | nVarChar | 254 | - |  |  |
| 3 | `OwnerId` | Owner ID | Int | 11 | - |  |  |
| 4 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 5 | `CreateTime` | Creation Time | Int | 11 | - |  |  |
| 6 | `IsPublic` | Is Public | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 7 | `TgtObject` | Target Object | nVarChar | 32 | - |  |  |
| 8 | `ApplyToDoc` | Apply to Additional Documents | nVarChar | 254 | - |  |  |
| 9 | `ViewType` | Type of Linked Object | nVarChar | 20 | - | DetailedViewHeader | `ListView` = List View<br>`DetailedViewHeader` = Detailed View Header<br>`DetailedViewRows` = Detailed View Rows |
| 10 | `Question` | Question Text | Text | 16 | - |  |  |
| 11 | `DataVers` | Data Version | Int | 11 | - | 1 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Id |
