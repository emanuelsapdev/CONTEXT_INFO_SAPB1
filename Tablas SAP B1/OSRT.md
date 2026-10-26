# OSRT - Korean Summary Report

- **Tabla:** OSRT
- **Descripción:** Korean Summary Report
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSRT.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Abstract ID | Int | 11 | - |  |  |
| 2 | `SumRptId` | Summary Report ID | nVarChar | 100 | - |  |  |
| 3 | `SumRptDate` | Summary Report Date | Date | 8 | - |  |  |
| 4 | `BPLId` | Business Place ID | Int | 11 | - |  |  |
| 5 | `FromDate` | From Date | Date | 8 | - |  |  |
| 6 | `ToDate` | To Date | Date | 8 | - |  |  |
| 7 | `RptType` | Report Type | VarChar | 1 | - | C | `V` = Vendor<br>`C` = Customer |
| 8 | `version` | Report Generation Version | nVarChar | 50 | - |  |  |
| 9 | `SumSubId` | Summary Report Sub ID | nVarChar | 254 | - |  |  |
| 10 | `SumRptType` | Summary Report Type | nVarChar | 254 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId |
| SUM_RPT_ID | Yes | SumRptId |
