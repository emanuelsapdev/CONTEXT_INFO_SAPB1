# OWEX - Workflow Engine Execution Entity

- **Tabla:** OWEX
- **Descripción:** Workflow Engine Execution Entity
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OWEX.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Id` | ID | Identity | 11 | - |  |  |
| 2 | `IsActive` | Is Active | Int | 6 | - |  |  |
| 3 | `IsConCurr` | Is Concurrent | Int | 6 | - |  |  |
| 4 | `IsScope` | Is Scope | Int | 6 | - |  |  |
| 5 | `ProcInstId` | Process Instance ID | nVarChar | 100 | - |  |  |
| 6 | `ParentId` | Parent ID | Int | 11 | - |  |  |
| 7 | `ProcDefId` | Process Definition ID | Int | 11 | - |  |  |
| 8 | `ActId` | Activity ID | nVarChar | 250 | - |  |  |
| 9 | `DataContex` | Data Context | Text | 16 | - |  |  |
| 10 | `B1WFInstId` | Workflow Instance ID | Int | 11 | - |  |  |
| 11 | `LastUpdate` | Last Update Date and Time | nVarChar | 50 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Id |
