# AWEX - Workflow Engine Execution Entity

- **Tabla:** AWEX
- **Descripción:** Workflow Engine Execution Entity
- **Cantidad de campos:** 13
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AWEX.html

## Campos (13)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Id` | ID | Int | 11 | - |  |  |
| 2 | `IsActive` | Is Active | Int | 6 | - |  |  |
| 3 | `IsConCurr` | Is Concurrent | Int | 6 | - |  |  |
| 4 | `IsScope` | Is Scope | Int | 6 | - |  |  |
| 5 | `ProcInstId` | Process Instance ID | nVarChar | 100 | - |  |  |
| 6 | `BizKey` | Business Key | nVarChar | 250 | - |  |  |
| 7 | `ParentId` | Parent ID | Int | 11 | - |  |  |
| 8 | `ProcDefId` | Process Definition ID | Int | 11 | - |  |  |
| 9 | `ActId` | Activity ID | nVarChar | 250 | - |  |  |
| 10 | `DataContex` | Data Context | Text | 16 | - |  |  |
| 11 | `B1WFInstId` | Workflow Instance ID | Int | 11 | - |  |  |
| 12 | `logInst` | Log Instance | Int | 11 | - |  |  |
| 13 | `LastUpdate` | Last Update Date | nVarChar | 50 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Id, logInst |
