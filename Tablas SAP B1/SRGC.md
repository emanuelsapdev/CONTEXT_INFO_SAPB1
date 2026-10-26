# SRGC - Registred companies

- **Tabla:** SRGC
- **Descripción:** Registred companies
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SRGC.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `dbName` | DB Name | nVarChar | 100 | - |  |  |
| 2 | `cmpName` | Comp. Name | nVarChar | 200 | - |  |  |
| 3 | `versStr` | Version | nVarChar | 13 | - |  |  |
| 4 | `dbUser` | SQL User | nVarChar | 50 | - |  |  |
| 5 | `LOC` | localization | nVarChar | 100 | - |  |  |
| 6 | `cmpStatus` | Comp. Status | VarChar | 1 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | dbName, dbUser |
