# SXRCO - XLR Context

- **Tabla:** SXRCO
- **Descripción:** XLR Context
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SXRCO.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ContextId` | ContextId | Int | 11 | - |  |  |
| 2 | `B1User` | B1User | nVarChar | 50 | - |  |  |
| 3 | `Password` | Password | nVarChar | 50 | - |  |  |
| 4 | `Language` | Language | Int | 11 | - |  |  |
| 5 | `Applicatio` | ApplicationId | Int | 11 | - |  |  |
| 6 | `LogonDate` | LogonDate | Date | 8 | - |  |  |
| 7 | `ExpiryDate` | ExpiryDate | Date | 8 | - |  |  |
| 8 | `Constrain` | Constraint | nVarChar | 250 | - |  |  |
| 9 | `DB` | DB | nVarChar | 250 | - |  |  |
| 10 | `ForceCust` | ForceCustomConnect | Int | 11 | - | 0 |  |
| 11 | `Roles` | Roles | nVarChar | 250 | - |  |  |
| 12 | `InvalidTer` | InvalidTerms | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ContextId |
