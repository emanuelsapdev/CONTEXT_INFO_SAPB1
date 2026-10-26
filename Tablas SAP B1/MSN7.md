# MSN7 - MRP Job Period Data

- **Tabla:** MSN7
- **Descripción:** MRP Job Period Data
- **Cantidad de campos:** 13
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MSN7.html

## Campos (13)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `JobID` | Job ID | Int | 11 | - |  |  |
| 2 | `ParentLn` | Parent Line Number | Int | 11 | - |  |  |
| 3 | `SeqNum` | Sequence Number | Int | 11 | - |  |  |
| 4 | `PeriodId` | Period ID | Int | 11 | - |  |  |
| 5 | `PrdDate` | Period Date | nVarChar | 8 | - |  |  |
| 6 | `Quantity` | Quantity | nVarChar | 50 | - |  |  |
| 7 | `IsRed` | Is Red | VarChar | 1 | - |  |  |
| 8 | `IsGrey` | Is Grey | VarChar | 1 | - |  |  |
| 9 | `IsLightGry` | Is Light Grey | VarChar | 1 | - |  |  |
| 10 | `Remark` | Remarks | nVarChar | 200 | - |  |  |
| 11 | `IsFuture` | Is Future Data | VarChar | 1 | - |  |  |
| 12 | `PegFlag` | Pegging Flag | VarChar | 1 | - |  |  |
| 13 | `PrvwEnbld` | Preview Enabled Flag | VarChar | 1 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | JobID, ParentLn, SeqNum |
