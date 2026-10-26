# OCSC - Crystal Server Configuration

- **Tabla:** OCSC
- **Descripción:** Crystal Server Configuration
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCSC.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | CSC Abs. Entry | Int | 11 | - |  |  |
| 2 | `Name` | Server Name | nVarChar | 100 | - |  |  |
| 3 | `User` | Logon User Code | nVarChar | 30 | - |  |  |
| 4 | `Password` | Logon User Password | nVarChar | 254 | - |  |  |
| 5 | `URL` | URL | nVarChar | 200 | - |  |  |
| 6 | `IsDefault` | Is Default | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 7 | `Port` | Port | nVarChar | 20 | - | 8080 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry |
