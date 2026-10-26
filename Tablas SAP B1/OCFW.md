# OCFW - Cash Flow Line Item

- **Tabla:** OCFW
- **Descripción:** Cash Flow Line Item
- **Cantidad de campos:** 14
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCFW.html

## Campos (14)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CFWId` | Cash Flow Line Item ID | Int | 11 | - |  |  |
| 2 | `CFWName` | Cash Flow Line Item Name | nVarChar | 200 | - |  |  |
| 3 | `LineNum` | Cash Flow Line No. | nVarChar | 5 | - |  |  |
| 4 | `Postable` | Cash Flow Item [Active/Title] | VarChar | 1 | - | Y | `Y` = Active Item<br>`N` = Header Item |
| 5 | `FatherNum` | Parent Item Key | Int | 11 | [OCFW](OCFW.md) |  |  |
| 6 | `Levels` | Cash Flow Item Level | Int | 6 | - | 3 |  |
| 7 | `GroupMask` | Group Mask | Int | 6 | - | 1 |  |
| 8 | `GroupLine` | Serial No. in Group | Int | 11 | - |  |  |
| 9 | `ExtrMatch` | External Reconciliation No. | Int | 11 | - |  |  |
| 10 | `IntrMatch` | Internal Reconciliation No. | Int | 11 | - |  |  |
| 11 | `RateDifCFW` | Rate Differences CFW | Int | 11 | - |  |  |
| 12 | `DataSource` | Data Source | Int | 6 | - |  |  |
| 13 | `Attr` | Attribute | Int | 6 | - |  |  |
| 14 | `Direction` | Direction | Int | 6 | - |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CFWId |
| INTER_KEY | No | FatherNum |
| INDEX_KEY | Yes | CFWName |
