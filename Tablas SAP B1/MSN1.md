# MSN1 - MRP Scenarios - Warehouses Array

- **Tabla:** MSN1
- **Descripción:** MRP Scenarios - Warehouses Array
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MSN1.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [OMSN](OMSN.md) |  |  |
| 2 | `WhsCode` | Warehouse Code | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 3 | `ReqSel` | Requirement Selection | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 4 | `InvtSel` | Inventory Selection | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 5 | `ExtIvntSel` | Existing Inventory Selection | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, WhsCode |
