# OSDT - AT Document Type

- **Tabla:** OSDT
- **Descripción:** AT Document Type
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSDT.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Code | nVarChar | 10 | - |  |  |
| 2 | `Desc` | Description | nVarChar | 200 | - |  |  |
| 3 | `Type` | Type | VarChar | 1 | - | T | `T` = Transfer<br>`I` = Invoice |
| 4 | `DataSource` | Data Source | VarChar | 1 | - | N |  |
| 5 | `UserSign` | User Signature | Int | 6 | - |  |  |
| 6 | `IsSys` | Is System | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code |
