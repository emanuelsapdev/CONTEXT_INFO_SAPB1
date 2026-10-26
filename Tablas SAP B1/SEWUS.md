# SEWUS - SEWUS

- **Tabla:** SEWUS
- **Descripción:** SEWUS
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SEWUS.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Absolute Entry | Int | 11 | - |  |  |
| 2 | `CompanyNam` | CompanyName | nVarChar | 200 | - |  |  |
| 3 | `SmpTableId` | Smp Table ID | nVarChar | 3 | - |  |  |
| 4 | `EwaSentDat` | EWA Sent Date | nVarChar | 10 | - |  |  |
| 5 | `CustNumber` | Customer Number | VarChar | 1 | - |  |  |
| 6 | `CompDbName` | Company DB Name | nVarChar | 200 | - |  |  |
| 7 | `EwaUserCod` | Ewa User Code | nVarChar | 16 | - |  |  |
| 8 | `EwaUserNam` | Ewa User Name | nVarChar | 16 | - |  |  |
| 9 | `EwaUserSup` | Ewa Is super user | VarChar | 1 | - | 0 | `1` = Yes<br>`0` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
