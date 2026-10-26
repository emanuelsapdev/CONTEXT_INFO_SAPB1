# CCS1 - Cycle Count Determination- Subtable

- **Tabla:** CCS1
- **Descripción:** Cycle Count Determination- Subtable
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CCS1.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WhsCode` | Warehouse Code | nVarChar | 8 | - |  |  |
| 2 | `Entry` | Entry | Int | 11 | - |  |  |
| 3 | `CycleCode` | Cycle Code | Int | 6 | - |  |  |
| 4 | `Alert` | Alert | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 5 | `DestUser` | Destination User | Int | 6 | - |  |  |
| 6 | `NextDate` | Next Counting Date | Date | 8 | - |  |  |
| 7 | `Time` | Time | Int | 6 | - |  |  |
| 8 | `ExcldZrQty` | Exclude Zero Quantity | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 9 | `Alerted` | Alerted | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 10 | `ChangExist` | Change Existing Items in DI | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WhsCode, Entry |
