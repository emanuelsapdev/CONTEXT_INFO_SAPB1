# DAB1 - Dashboard Queries

- **Tabla:** DAB1
- **Descripción:** Dashboard Queries
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/DAB1.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DsbEntry` | Dashboard Entry | Int | 11 | [ODAB](ODAB.md) |  |  |
| 2 | `QryCtgry` | Query Category | Int | 11 | [OQCN](OQCN.md) |  |  |
| 3 | `QryName` | Query Name | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DsbEntry, QryCtgry, QryName |
