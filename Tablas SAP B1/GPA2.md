# GPA2 - Gross Profit Adjustments - Parameters

- **Tabla:** GPA2
- **Descripción:** Gross Profit Adjustments - Parameters
- **Cantidad de campos:** 13
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/GPA2.html

## Campos (13)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | - |  |  |
| 2 | `Name` | Wizard Parameters Name | nVarChar | 100 | - |  |  |
| 3 | `Descript` | Wizard Parameters Description | nVarChar | 100 | - |  |  |
| 4 | `PostDateFr` | Sales Doc. Posting Date From | Date | 8 | - |  |  |
| 5 | `PostDateTo` | Sales Doc. Posting Date To | Date | 8 | - |  |  |
| 6 | `ItemCodeFr` | Item No. From | nVarChar | 50 | - |  |  |
| 7 | `ItemCodeTo` | Item No. To | nVarChar | 50 | - |  |  |
| 8 | `ItmsGrpCod` | Item Group | Int | 6 | [OITB](OITB.md) | 100 |  |
| 9 | `AdditFilt` | Additional Filters | VarChar | 1 | - |  |  |
| 10 | `SearchCond` | Find Items Search Condition | VarChar | 1 | - |  |  |
| 11 | `PropList` | Item Properties List | nVarChar | 100 | - |  |  |
| 12 | `DisplInact` | Display Inactive Items | VarChar | 1 | - |  |  |
| 13 | `UseGroups` | Find items with only the selected properties | VarChar | 1 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
