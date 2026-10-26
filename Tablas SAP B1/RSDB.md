# RSDB - Resource DB List

- **Tabla:** RSDB
- **Descripción:** Resource DB List
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RSDB.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsKey` | Abs Key | Int | 11 | - |  |  |
| 2 | `ServerName` | Server Name | nVarChar | 254 | - |  |  |
| 3 | `DbName` | Resource DB Name | nVarChar | 64 | - |  |  |
| 4 | `Date` | Creation date | Date | 8 | - |  |  |
| 5 | `Time` | Creation Time | Date | 8 | - |  |  |
| 6 | `OrigDB` | Original DB | Int | 11 | - |  |  |
| 7 | `MBServer` | Master Base Server Name | nVarChar | 254 | - |  |  |
| 8 | `MBDbName` | Master Base DB Name | nVarChar | 64 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsKey |
| SERVER_DB | Yes | ServerName, DbName |
