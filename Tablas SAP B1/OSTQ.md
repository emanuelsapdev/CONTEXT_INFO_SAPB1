# OSTQ - Inventory Valuation Utility Queries

- **Tabla:** OSTQ
- **Descripción:** Inventory Valuation Utility Queries
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSTQ.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `QueryNAme` | Query Name | nVarChar | 100 | - |  |  |
| 3 | `QueryStr` | Query String | Text | 16 | - |  |  |
| 4 | `Severity` | Inventory Valuation Query Seve | VarChar | 1 | - | E | `W` = Warning if fails<br>`E` = Error if fails |
| 5 | `QueryGroup` | Query Group | VarChar | 1 | - | B | `B` = Before Recalculation<br>`A` = After Recalculation<br>`T` = Year Transfer |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
