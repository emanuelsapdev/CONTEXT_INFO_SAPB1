# OWJB - Workflow Job Entity

- **Tabla:** OWJB
- **Descripción:** Workflow Job Entity
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OWJB.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Id` | ID | Int | 11 | - |  |  |
| 2 | `HandlerTyp` | Handler Type | nVarChar | 50 | - |  |  |
| 3 | `ExecId` | Execution ID | Int | 11 | - |  |  |
| 4 | `Rev` | Revision | Int | 11 | - |  |  |
| 5 | `DueDate` | Due Date | Date | 8 | - |  |  |
| 6 | `ProcInstId` | Process Instance ID | Int | 11 | - |  |  |
| 7 | `Type` | Type | nVarChar | 250 | - |  |  |
| 8 | `HandlerCfg` | Handler Configuration | nVarChar | 250 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Id |
