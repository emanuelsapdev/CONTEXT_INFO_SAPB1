# OWSV - Web Client Linked View

- **Tabla:** OWSV
- **Descripción:** Web Client Linked View
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OWSV.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Guid` | GUID | nVarChar | 40 | - |  |  |
| 2 | `Name` | Name | nVarChar | 254 | - |  |  |
| 3 | `OwnerId` | Owner ID | Int | 11 | - |  |  |
| 4 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 5 | `CreateTime` | Creation Time | Int | 11 | - |  |  |
| 6 | `IsPublic` | Is Public | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 7 | `TgtObject` | Target Object | nVarChar | 32 | - |  |  |
| 8 | `VariantId` | Variant ID | nVarChar | 40 | - |  |  |
| 9 | `ApplyToDoc` | Apply To Docs | nVarChar | 254 | - |  |  |
| 10 | `ViewType` | Type of Linked View | nVarChar | 20 | - | DetailedViewHeader | `ListView` = List View<br>`DetailedViewHeader` = Detailed View Header<br>`DetailedViewRows` = Detailed View Rows |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Guid |
