# OWIN - Workflow Engine Information

- **Tabla:** OWIN
- **Descripción:** Workflow Engine Information
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OWIN.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Id` | ID | Int | 11 | - |  |  |
| 2 | `WFInstId` | Workflow Instance ID | Int | 11 | - |  |  |
| 3 | `TaskId` | Task ID | Int | 11 | - |  |  |
| 4 | `ProcDefId` | Process Definition ID | nVarChar | 250 | - |  |  |
| 5 | `FlowElemId` | Flow Element ID | nVarChar | 250 | - |  |  |
| 6 | `InfoType` | Information Type | nVarChar | 2 | - |  | `E` = Error<br>`W` = Warning<br>`I` = Information<br>`O` = Other |
| 7 | `InfoCode` | Predefined Information Code | nVarChar | 10 | - |  |  |
| 8 | `Desc` | Description | Text | 16 | - |  |  |
| 9 | `CreateDate` | Create Date | Date | 8 | - |  |  |
| 10 | `CreateTime` | Create Time | Int | 11 | - |  |  |
| 11 | `IsRead` | Info. read by SAP Business One? | VarChar | 1 | - |  | `N` = No<br>`Y` = Yes |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Id |
