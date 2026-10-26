# OUDV - User-Defined Views for Service Layer

- **Tabla:** OUDV
- **Descripción:** User-Defined Views for Service Layer
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OUDV.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Name` | View Name | nVarChar | 100 | - |  |  |
| 2 | `DBType` | Database Type | nVarChar | 20 | - |  | `MSSQL` = Microsoft SQL Server<br>`HANA` = SAP HANA |
| 3 | `SchemaName` | Schema Name | nVarChar | 64 | - |  |  |
| 4 | `CreateDate` | Create Date | Date | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Name |
