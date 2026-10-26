# OSQL - SQL query

- **Tabla:** OSQL
- **Descripción:** SQL query
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSQL.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `SqlCode` | SQL query code | nVarChar | 254 | - |  |  |
| 2 | `SqlName` | SQL query name | nVarChar | 254 | - |  |  |
| 3 | `SqlText` | SQL text | Text | 16 | - |  |  |
| 4 | `ParamList` | List of bound parameter names | nVarChar | 254 | - |  |  |
| 5 | `ParamDetai` | Parameter details | nVarChar | 254 | - |  |  |
| 6 | `InternalS` | Internal SQL text | Text | 16 | - |  |  |
| 7 | `LogInstanc` | Log instance | Int | 11 | - | 0 |  |
| 8 | `ObjType` | Object Type | nVarChar | 20 | - | 2 |  |
| 9 | `CreateDate` | Created On | Date | 8 | - |  |  |
| 10 | `UpdateDate` | Updated On | Date | 8 | - |  |  |
| 11 | `DataVers` | Data version | Int | 11 | - | 1 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | SqlCode |
