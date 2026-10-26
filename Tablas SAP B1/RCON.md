# RCON - Connection Map for CR Templates

- **Tabla:** RCON
- **Descripción:** Connection Map for CR Templates
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RCON.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocCode` | Internal Template Key | nVarChar | 8 | - |  |  |
| 2 | `ConnID` | Connection ID | Int | 11 | - |  |  |
| 3 | `OldServer` | Old Server Name | nVarChar | 64 | - |  |  |
| 4 | `OldDbName` | Old Database Name | nVarChar | 64 | - |  |  |
| 5 | `NewServer` | Mapped Server Name | nVarChar | 64 | - |  |  |
| 6 | `NewDbName` | Mapped Database Name | nVarChar | 64 | - |  |  |
| 7 | `UserCode` | User Code | nVarChar | 32 | - |  |  |
| 8 | `SubIndex` | Subreport Index | Int | 6 | - |  |  |
| 9 | `SubName` | Subreport Name | nVarChar | 64 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocCode, ConnID |
