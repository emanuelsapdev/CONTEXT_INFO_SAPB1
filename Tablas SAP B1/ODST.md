# ODST - Static Data Source

- **Tabla:** ODST
- **Descripción:** Static Data Source
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ODST.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Id` | UUID string | nVarChar | 64 | - |  |  |
| 2 | `Owner` | Owner ID | Int | 6 | - |  |  |
| 3 | `DataSouId` | ID of data source meta | nVarChar | 128 | - |  |  |
| 4 | `PermId` | Permission id of data source | Int | 11 | - |  |  |
| 5 | `MetaVer` | Version of data source meta | Int | 11 | - |  |  |
| 6 | `Type` | Type | Int | 11 | - |  |  |
| 7 | `Dependency` | Dependency | Text | 16 | - |  |  |
| 8 | `Category` | Category | Text | 16 | - |  |  |
| 9 | `MetaCont` | Json string of datasource meta | Text | 16 | - |  |  |
| 10 | `Status` | 0-no view, 1- view created... | Int | 11 | - |  |  |
| 11 | `LastUpdate` | Timestamp | nVarChar | 64 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Id |
| SOURCEID | Yes | DataSouId |
