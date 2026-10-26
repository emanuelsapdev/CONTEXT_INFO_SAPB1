# BAL1 - Opening Balance Instances

- **Tabla:** BAL1
- **Descripción:** Opening Balance Instances
- **Cantidad de campos:** 14
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/BAL1.html

## Campos (14)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `Instance` | Instance | Int | 11 | - |  |  |
| 3 | `OBDate` | Date of Opening Balance (first day of next fiscal period) | Date | 8 | - |  |  |
| 4 | `InAmount` | Total Received Value | Num | 19.6 | - |  |  |
| 5 | `InQty` | Total Received Quantity | Num | 19.6 | - |  |  |
| 6 | `OutQty` | Total Issued Quantity | Num | 19.6 | - |  |  |
| 7 | `InAmntLWA` | Last Non-zero Total Received Value | Num | 19.6 | - |  |  |
| 8 | `InQtyLWA` | Last Non-zero Total Received Quantity | Num | 19.6 | - |  |  |
| 9 | `LastTrnsID` | Last Transaction ID | Int | 11 | - |  |  |
| 10 | `WasPrevOB` | OB from Start of Fiscal Year | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 11 | `CreateDate` | Create Date | Date | 8 | - |  |  |
| 12 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 13 | `CrossPRev` | Cross Period Revaluation from Next Period | Num | 19.6 | - |  |  |
| 14 | `WasUpdPrCB` | Update previous Closing Balance with cross period revaluations | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, Instance |
