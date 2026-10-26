# BOLG - BO Audit Log

- **Tabla:** BOLG
- **Descripción:** BO Audit Log
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/BOLG.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Id` | ID | nVarChar | 40 | - |  |  |
| 2 | `CompanyId` | CompanyId | nVarChar | 32 | - |  |  |
| 3 | `UserName` | User Name | nVarChar | 128 | - |  |  |
| 4 | `B1UserCode` | B1UserCode | nVarChar | 32 | - |  |  |
| 5 | `SourceIp` | SourceIp | nVarChar | 45 | - |  |  |
| 6 | `ComponenId` | ComponentId | nVarChar | 96 | - |  |  |
| 7 | `ActionTs` | ActionTimestamp | nVarChar | 32 | - |  |  |
| 8 | `Category` | Category | nVarChar | 32 | - |  |  |
| 9 | `SubCategry` | SubCategory | nVarChar | 32 | - |  |  |
| 10 | `ActionMsg` | ActionMessage | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Id |
