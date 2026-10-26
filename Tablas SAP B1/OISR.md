# OISR - Service Calls

- **Tabla:** OISR
- **Descripción:** Service Calls
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OISR.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `RequestNum` | Request No. | Int | 11 | - |  |  |
| 2 | `Open_Date` | Start Date | Date | 8 | - |  |  |
| 3 | `Open_Time` | Start Time | Int | 11 | - |  |  |
| 4 | `Task_Id` | Request No. in SAP Business One | Int | 11 | - |  |  |
| 5 | `Contact` | Contact Person | nVarChar | 30 | - |  |  |
| 6 | `Phone` | Telephone | nVarChar | 20 | - |  |  |
| 7 | `TaskType` | Request Type | Int | 6 | - | 0 | `0` = Explanation<br>`1` = Error<br>`2` = Complaints |
| 8 | `Dscription` | Call Description | nVarChar | 254 | - |  |  |
| 9 | `Answer` | Troubleshooting | Text | 16 | - |  |  |
| 10 | `Status` | Call Status | VarChar | 1 | - | O | `O` = Open<br>`C` = Closed |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | RequestNum |
