# SEWH1 - SEWH1

- **Tabla:** SEWH1
- **Descripción:** SEWH1
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SEWH1.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `MachineNam` | Machine Name | nVarChar | 254 | - |  |  |
| 2 | `CompDbNam` | Company Db Name | nVarChar | 200 | - |  |  |
| 3 | `ID` | AddOn ID | Int | 11 | - |  |  |
| 4 | `Name` | AddOn Name | nVarChar | 40 | - |  |  |
| 5 | `Version` | AddOn Version | nVarChar | 13 | - |  |  |
| 6 | `Status` | AddOn Status | nVarChar | 50 | - |  |  |
| 7 | `InstStatus` | AddOn Installation Status | VarChar | 1 | - | P | `I` = Installed<br>`P` = Pending |
| 8 | `EwaSentDat` | EWA Sent Date | nVarChar | 10 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | MachineNam, CompDbNam, ID |
